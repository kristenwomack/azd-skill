# Awesome AZD Submission Process Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile and submission stage. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-006
    version: 2
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited submission requirement using the catalog's explicit local evidence criteria.
    severity: collection-required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; only recorded checks establish validation coverage.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/publishing-guidelines.md#4-submit-to-awesome-azd
    title: Submission process
    requirement: Awesome AZD submissions MUST use one of the submission-authority paths.
    applies: public-awesome-azd profile at the explicitly selected submission stage; never preparation.
    inspect: Submission pull request or automated template-submission issue.
    pass: Readable submission evidence is a direct Awesome AZD pull request or automated template-submission issue.
    fail: Readable submission evidence uses neither submission-authority path.
    unknown: Submission evidence is absent or unreadable.
    remediation: Use a direct Awesome AZD pull request or the automated template-submission issue.
    layer: destination
    stages:
      - submission
```
