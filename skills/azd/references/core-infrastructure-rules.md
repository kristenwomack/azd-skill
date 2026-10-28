# Core Infrastructure Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

All rules below have `status: active`, `policy_kind: approved`, and `severity: required`. Source mappings and local interpretation are defined in [policy-sources.md](policy-sources.md); shared terms and evidence handling are in [core-evaluation-terms.md](core-evaluation-terms.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-CORE-003
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
    title: Infrastructure assets
    requirement: Infrastructure assets appropriate to the template scenario MUST be committed.
    applies: Any azd template repository.
    inspect: Scenario docs, azure.yaml infra configuration, and tracked infrastructure assets.
    pass: Scenario documentation names the provisioned resource types, the configured or default infrastructure path is resolved, and tracked files under that path declare each named resource type.
    fail: Readable scenario documentation names a provisioned resource type that is absent from the readable tracked files under the resolved infrastructure path, or a required infrastructure file is untracked.
    unknown: Scenario documentation or azure.yaml is unreadable, provisioned resource types are not stated, the configured or default infrastructure path cannot be resolved, or tracked-file state cannot be read.
    remediation: Commit the infrastructure assets required by the documented scenario.
    layer: core
    stages:
      - preparation
      - submission
  - id: AZD-CORE-004
    version: 1
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited core requirement using the catalog's explicit local evidence criteria.
    severity: required
    source_revision: 22de60335bd77269a2e952cd0e3e8fab56ed4aa1
    requirement_kind: upstream-guidance
    local_evidence_policy: Use policy-sources.md safeguards; insufficient evidence is uncertainty, not an upstream defect.
    references:
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/docs/readme.md#core-azd-template-requirements
    title: Documented azd up path contents
    requirement: The repository MUST include readable documentation for its azd up path and every code or configuration path that documentation identifies.
    applies: Any azd template repository.
    inspect: Documented azd up path and referenced code and configuration.
    pass: Readable tracked documentation states the azd up sequence and names its code and configuration paths, and every named path is present, tracked, and readable.
    fail: The documented path references a required component proven absent.
    unknown: The documented azd up path is unreadable or does not name its required code and configuration, or repository file state cannot be read.
    remediation: Add or correct the azd up documentation and each code or configuration path it identifies.
    layer: core
    stages:
      - preparation
      - submission
```
