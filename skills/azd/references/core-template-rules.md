# Core Template Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

All rules below have `status: active`, `policy_kind: approved`, and `severity: required`. Source mappings and local interpretation are defined in [policy-sources.md](policy-sources.md); shared terms and evidence handling are in [core-evaluation-terms.md](core-evaluation-terms.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-CORE-001
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
      - https://github.com/Azure-Samples/azd-template-artifacts/blob/22de60335bd77269a2e952cd0e3e8fab56ed4aa1/publishing-guidelines.md#1-build-an-azd-compatible-repository
    title: Root azure.yaml
    requirement: azure.yaml MUST exist at the resolved template root.
    applies: Any azd template repository.
    inspect: Explicit target selection or documented working directory and its root file listing.
    pass: A readable root azure.yaml exists.
    fail: A readable root listing proves azure.yaml is absent.
    unknown: The root listing is inaccessible or template root is unresolved.
    remediation: Add azure.yaml at the resolved template root, or clarify the documented working directory.
    layer: core
    stages:
      - preparation
      - submission
  - id: AZD-CORE-002
    version: 2
    status: active
    policy_kind: approved
    authority: azd repository-owned catalog
    rationale: Tests the cited core requirement using the catalog's explicit local evidence criteria.
    severity: required
    source_revision: live-platform-reference; record inspected schema retrieval time and version or digest when supplied
    requirement_kind: platform-constraint
    local_evidence_policy: Use policy-sources.md safeguards; insufficient evidence is uncertainty, not an upstream defect.
    references:
      - https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/azd-schema
      - https://aka.ms/azure.yaml.json
    title: azd schema conformance
    requirement: azure.yaml MUST conform to the applicable azd schema defined above.
    applies: Any azd template repository.
    inspect: Template-root azure.yaml, the recorded machine-schema URL and retrieval time, and validator output for that schema.
    pass: Validator output identifies the applicable-schema URL and reports no schema errors for the inspected azure.yaml.
    fail: Validator output identifies the applicable-schema URL and reports one or more schema errors for the inspected azure.yaml.
    unknown: azure.yaml or the applicable schema is unreadable, or validator output tied to both is absent.
    remediation: Correct the reported errors against the applicable azd schema.
    layer: core
    stages:
      - preparation
      - submission
```
