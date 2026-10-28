# Awesome AZD Security Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-008
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
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#review-and-publication-readiness
    title: Security validation result
    requirement: The security validation MUST pass without warnings.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Supplied or readable security validation output that identifies the audited commit.
    pass: A readable security validation record identifies the audited commit and reports the analysis completing with no warnings and no errors.
    fail: A readable security validation record identifies the audited commit and reports one or more warnings or errors.
    unknown: No security validation record identifies the audited commit, a cited record is unreadable, or the cited run did not perform the security analysis.
    remediation: Resolve the reported security findings, such as using Microsoft Entra ID or a managed identity where supported and removing exposed secrets, then re-run the validation outside this read-only audit.
    layer: destination
    stages:
      - preparation
      - submission
```
