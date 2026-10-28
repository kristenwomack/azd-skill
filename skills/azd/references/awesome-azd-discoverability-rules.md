# Awesome AZD Discoverability Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-003
    version: 2
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
    title: Repository discoverability
    requirement: The repository description MUST state the deployed scenario, and topics MUST include the required repository topics plus at least one language, model, or technology topic that describes the template.
    applies: Explicit Awesome AZD publication readiness.
    inspect: GitHub repository description and topics, plus README.md or azure.yaml for scenario, language, model, and technology terms.
    pass: The non-empty description states the deployed scenario, and the topics include azd-templates and ai-azd-templates plus at least one language, model, or technology term present in README.md or azure.yaml.
    fail: Readable metadata shows an empty description, no topics, topics that omit azd-templates or ai-azd-templates, or no language, model, or technology topic.
    unknown: Repository metadata, README.md, or azure.yaml is unreadable, or the description and topics cannot be compared with repository evidence.
    remediation: Set a repository description that states the scenario, and add the required repository topics plus the language, model, and technology topics the template uses.
    layer: destination
    stages:
      - preparation
      - submission
```
