# Catalog Rule Schema

The following is this project's catalog structure, not an azd or organization
policy standard. Each bundled rule must define:

| Field | Required | Meaning |
|---|---:|---|
| `id` | yes | Stable unique identifier. |
| `title` | yes | Short requirement name. |
| `version` | yes | Rule revision. |
| `status` | yes | `active`, `inactive`, or `deprecated`. |
| `policy_kind` | yes | `approved`, `placeholder`, or `example`. |
| `authority` | yes | Owning policy source or `none` for examples. |
| `requirement` | yes | Exact normative requirement. |
| `rationale` | yes | Why the approved rule exists. |
| `applies_when` | yes | Explicit target conditions, including exclusions. |
| `evidence` | yes | Read-only locations or fields to inspect. |
| `pass_when` | yes | Deterministic sufficient condition for pass. |
| `fail_when` | yes | Deterministic sufficient condition for fail. |
| `unknown_when` | yes | Missing or ambiguous evidence conditions. |
| `severity` | yes | Catalog-defined impact label. |
| `remediation` | yes | Proposed corrective action; never auto-apply. |
| `references` | yes | Policy citations or an empty list. |
| `source_revision` | yes | Pinned source revision or explicit live-reference designation. |
| `requirement_kind` | yes | `upstream-guidance` or `platform-constraint`. |
| `local_evidence_policy` | yes | Local safeguards, distinct from upstream requirements. |
| `metadata` | no | Extensible owner, tags, dates, or notes map. |

Rules may add fields, but additions cannot weaken authority, evidence,
uncertainty, or read-only constraints. Rule order does not imply priority. Rule
views use `applies`, `inspect`, `pass`, `fail`, and `unknown` as short keys for
the corresponding schema fields.
