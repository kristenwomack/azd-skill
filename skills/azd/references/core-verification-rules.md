# Core Verification Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

All rules below have `status: active`, `policy_kind: approved`, and `severity: required`. Source mappings and local interpretation are defined in [policy-sources.md](policy-sources.md); shared terms and evidence handling are in [core-evaluation-terms.md](core-evaluation-terms.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-CORE-005
    version: 2
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited core requirement using the catalog's explicit local evidence criteria.
    severity: required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; insufficient evidence is uncertainty, not an upstream defect.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#core-azd-functionality
    title: Successful azd up verification
    requirement: The documented azd up happy path MUST have been executed successfully.
    applies: Any azd template repository.
    inspect: Supplied or readable workflow run, validation record, log, PR evidence, or manual verification record that identifies the audited commit and documented azd up path.
    pass: Evidence identifies the audited commit and documented azd up path and records a successful execution; no evidence for that commit records a failure.
    fail: Evidence identifying the audited commit and documented azd up path records a failed execution.
    unknown: No execution record identifies both the audited commit and documented azd up path, or a cited record is unreadable.
    remediation: Run the documented happy path outside this read-only audit and retain reviewable evidence.
    layer: core
    stages:
      - preparation
      - submission
  - id: AZD-CORE-006
    version: 2
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited core requirement using the catalog's explicit local evidence criteria.
    severity: required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; insufficient evidence is uncertainty, not an upstream defect.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/development-guidelines/definition-of-done.md#core-azd-functionality
    title: Verified teardown
    requirement: If the template provisions Azure resources, its documented teardown path MUST be verified using azd down or an explicitly documented equivalent.
    applies: Templates that provision Azure resources.
    inspect: Provisioning docs, teardown docs, and supplied or readable verification evidence.
    pass: Provisioning documentation states that Azure resources are created, names azd down or an explicit equivalent, and evidence identifying the audited commit records successful teardown with that path.
    fail: Evidence proves the documented teardown path fails or no teardown path is documented.
    unknown: Provisioning documentation is unreadable or does not state whether Azure resources are created, or no readable teardown record identifies the audited commit and documented path.
    remediation: Document and verify azd down or an explicit equivalent outside this read-only audit.
    layer: core
    stages:
      - preparation
      - submission
```
