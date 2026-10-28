# Local Evidence Safeguards

These are decisions owned by this catalog, not additional upstream mandates:

- Tie execution, security, and validation evidence to the inspected commit.
  Record working-tree state; evidence for HEAD does not verify uncommitted
  changes. If changes could affect a check, its historical result cannot
  establish PASS for the changed target. Report the evidence gap.
- Map readable scenario documentation to tracked resource declarations when
  establishing infrastructure fit. Resolve omitted `infra.path` to azd's
  default `infra` directory relative to the template root; omission is not a defect.
- Require documented component paths and a scenario-describing repository
  description with at least one matching technology topic to make broader
  usability/discoverability guidance deterministic. These are local evidence
  criteria, not verbatim upstream requirements.
- Require reviewable validator output identifying the actual schema and target.
  Record schema retrieval time and supplied version or digest; do not invent one.
  A documentation URL alone does not identify a machine schema.
- A relevant recorded failure takes precedence over success for the same target
  revision. An unrelated failing check does not establish a catalog failure.

If a safeguard prevents a conclusion, label it a local evidence limitation, not
an upstream rejection or proven defect.
