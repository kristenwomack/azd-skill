# Verified Submission Flow

Read-only GitHub API verification on 2026-10-15 pinned `Azure/awesome-azd` HEAD
[`c463284b7c756047e8732832f0ca65b85e37f24e`](https://github.com/Azure/awesome-azd/tree/c463284b7c756047e8732832f0ca65b85e37f24e).
This newer flow supersedes the older blanket metadata interpretation for rule
005 only; other rules retain their listed baseline.

- [Issue form](https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/.github/ISSUE_TEMPLATE/template-submission.yml):
  only Source Repository is required. Other fields are optional overrides.
- [Workflow](https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/.github/workflows/template-submission.yml)
  extracts metadata and creates a PR. Inspect the generated entry once available;
  do not fail issue preparation for fields the workflow will generate.
- [Entry writer](https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/website/scripts/update-templates-json.js)
  generates a UUID, requires an author URL, allows empty preview and IaC, and
  adds language/framework/service arrays only when non-empty.
- [Contributor guide](https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/website/docs/contribute.md#submit-a-pr)
  lists direct-entry title, description, attribution name/link, source, tags, and
  unique UUID. Check the prepared/final entry, not an issue-input checklist.
- [Schema reference](https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/docs/templates-schema.md)
  requires non-empty title, description, author, GitHub source, and recognized
  tags; preview and category arrays are optional. It treats authorUrl as optional,
  unlike the writer and contributor guide. The guide also lists an image.

**Catalog interpretation:** retain attribution link and UUID for PR entries,
require only applicable categories, and label preview **Recommended** for both
paths. Do not claim every upstream document agrees or that PASS guarantees
acceptance. Unknown applicability or inaccessible entries remain uncertain;
preview absence or access never changes a finding.
