# Awesome AZD Heading Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-007
    version: 3
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited submission requirement using the catalog's explicit local evidence criteria.
    severity: collection-required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; only recorded checks establish validation coverage.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#awesome-azd-repository-baseline
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#should
    title: Required README headings
    requirement: README.md MUST contain each required README heading as an H2 heading.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Template-root README.md heading structure, or a validation record identifying the audited revision and each H2 heading it checked.
    pass: Readable README.md contains every required README heading as an H2 heading, or a fresh validation record explicitly confirms every required H2 heading for that README; no fresh readable evidence contradicts that result.
    fail: A readable listing proves README.md is absent, readable README.md omits a required README heading or carries one only at another heading level, or a fresh record explicitly proves a required H2 heading is absent.
    unknown: README.md is unreadable and no fresh validation record establishes the complete required heading set, including Important Security Notice.
    remediation: Add the missing H2 headings to README.md and move existing content under the matching heading.
    layer: destination
    stages:
      - preparation
      - submission
```
