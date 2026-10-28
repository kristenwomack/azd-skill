# Awesome AZD Governance Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-002
    version: 1
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited publication requirement using the catalog's explicit local evidence criteria.
    severity: collection-required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; validator defaults do not replace the pinned guidance.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#awesome-azd-repository-baseline
    title: OSS governance files
    requirement: LICENSE.md, SECURITY.md, CONTRIBUTING.md, .github/CODE_OF_CONDUCT.md, and an issue template MUST be present.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Root and .github file listings.
    pass: Every named artifact and at least one issue template are present.
    fail: A readable listing proves any required artifact absent.
    unknown: Required listings are inaccessible.
    remediation: Add the missing baseline OSS or governance artifacts.
    layer: destination
    stages:
      - preparation
      - submission
```
