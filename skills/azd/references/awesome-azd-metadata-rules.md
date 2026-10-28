# Awesome AZD Metadata Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile. Preparation excludes AZD-AWESOME-006. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-005
    version: 2
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited submission requirement using the catalog's explicit local evidence criteria.
    severity: collection-required
    source_revision: c463284b7c756047e8732832f0ca65b85e37f24e
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; only recorded checks establish validation coverage.
    references:
      - https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/.github/ISSUE_TEMPLATE/template-submission.yml
      - https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/.github/workflows/template-submission.yml
      - https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/website/scripts/update-templates-json.js
      - https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/website/docs/contribute.md
      - https://github.com/Azure/awesome-azd/blob/c463284b7c756047e8732832f0ca65b85e37f24e/docs/templates-schema.md
    title: Path-appropriate gallery metadata
    requirement: Metadata MUST match the selected submission path and stage. Automated issue preparation requires only a GitHub source repository URL; other fields are optional overrides. For an automated generated PR, inspect the generated gallery entry. Direct PR preparation/submission requires the final entry's title, description, author, authorUrl, GitHub source, non-empty recognized tags, and unique UUID. Require only applicable language/framework/Azure-service/IaC categories. A preview image is Recommended, never mandatory.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Selected automated-issue or direct-PR path, preparation/submission stage, issue inputs or final website/static/templates.json entry, and category applicability. Generated PR entries use title, description, author, authorUrl, source, tags and id; the workflow generates the UUID and may omit preview or inapplicable categories.
    pass: Automated issue preparation (or a submitted issue awaiting generation) supplies a GitHub repository URL without requiring overrides or a caller-provided UUID. Once a generated PR is available, its entry has non-empty title, description, author, authorUrl, GitHub source, recognized tags, a unique valid UUID, and applicable metadata categories. A direct PR's prepared/final entry satisfies those same entry criteria. No preview or inapplicable category is required.
    fail: Readable path-appropriate data proves a required source URL missing/invalid, or a final/prepared PR entry lacks a required field, contains an invalid/duplicate UUID or unrecognized tag, or omits a category known to apply. Missing preview or optional issue overrides never fails.
    unknown: Submission path/stage, required inputs, generated entry, UUID uniqueness evidence, or relevant category applicability cannot be determined. An expected generated PR that is inaccessible is uncertainty, not proof of missing fields. Preview access does not affect the verdict.
    remediation: Supply the required repository URL for the automated issue, or correct the required final PR metadata and applicable categories. Recommend a preview separately; do not require optional overrides.
    layer: destination
    stages:
      - preparation
      - submission
```
