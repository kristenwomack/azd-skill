# Core Evaluation Terms

Shared definitions for the core rule views indexed by
[compliance-rules.md](compliance-rules.md).

- **Template root:** the explicitly selected or documented azd working
  directory, otherwise the repository root. Rule paths are relative to it.
  An unresolved or ambiguous root is an evidence gap, not proof of a missing file.
- **Applicable azd schema:** the machine-readable schema linked by the
  [platform reference](https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/azd-schema),
  `https://aka.ms/azure.yaml.json`. Record its URL (and resolved URL when
  available), retrieval time, and supplied version or digest. The Learn page is
  documentation, not the schema. Without readable schema validation evidence,
  conformance is `UNABLE TO DETERMINE`.
- **Audited commit:** the target repository commit named in the report.
  Execution evidence is fresh only when it identifies that commit; evidence
  from another commit or before relevant uncommitted changes is insufficient.
- **Scenario-fit evidence:** readable scenario documentation names provisioned
  resource types, the infrastructure path resolves from `azure.yaml` or its
  default `infra`, and tracked files there declare those types. Explicit
  `infra.path` is not required; framework-specific equivalents are acceptable.
  Mapping named types to tracked declarations is a local evidence safeguard,
  not upstream wording. If required evidence is unreadable, fit is
  `UNABLE TO DETERMINE`.
- When fresh records disagree, a recorded failure takes precedence over
  success. If a required file, external record, or authority cannot be read,
  use the rule's `unknown` outcome; do not infer its contents.
