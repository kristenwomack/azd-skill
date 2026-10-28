# Awesome AZD Publication Rules

Authority: this repository-owned rule module, as indexed by [compliance-rules.md](compliance-rules.md).

Apply only to the explicitly selected `public-awesome-azd` profile, in preparation or submission. Interpret defined terms using [awesome-azd-rules.md](awesome-azd-rules.md).

<!-- Generated from policy/publication-catalog.json; run npm run catalog:generate. Do not edit. -->

```yaml
rules:
  - id: AZD-AWESOME-001
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
    title: Publication README
    requirement: README.md MUST explain the scenario, prerequisites, deployment steps, verification steps, and cleanup guidance.
    applies: Explicit Awesome AZD publication readiness.
    inspect: Root README.md.
    pass: README.md names the deployed scenario, states prerequisites or that there are none, gives deployment commands, gives a verification action and expected result, and gives a cleanup command or procedure.
    fail: A readable README is absent or one or more topics are absent.
    unknown: README.md is unreadable or its text does not distinguish one or more required topics.
    remediation: Add the missing publication-readiness topics to README.md.
    layer: destination
    stages:
      - preparation
      - submission
```
