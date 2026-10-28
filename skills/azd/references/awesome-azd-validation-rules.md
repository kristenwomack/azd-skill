# Awesome AZD Validation Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-004
    version: 3
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited publication requirement using the catalog's explicit local evidence criteria.
    severity: collection-required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; validator defaults do not replace the pinned guidance.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#review-and-publication-readiness
    title: Reviewable validation evidence
    requirement: Reviewers MUST be able to access evidence of a successful validation, test, or manual verification that identifies the audited commit.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Supplied or linked PRs, workflow runs, screenshots, or logs, including the checks each record states it performed.
    pass: A readable record identifies the audited commit and a successful validation, test, or manual verification; no record for that commit reports a failure of a check that maps to an active rule.
    fail: A readable record identifying the audited commit reports a failed check that maps to an active rule in this catalog.
    unknown: No supplied record identifies the audited commit, a cited record is unreadable, or the only failing record's checks map to no active rule.
    remediation: Produce and retain readable successful validation evidence for the audited commit outside this read-only audit.
    layer: destination
    stages:
      - preparation
      - submission
```
