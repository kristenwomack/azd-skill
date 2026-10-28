# Compliance Rule Catalog

The canonical bundled policy is [publication-catalog.json](../policy/publication-catalog.json). This index and
the generated rule views support human review and manual fallback; the normal
audit uses the checker's profile-filtered payload instead of loading all modules.
Enforce only entries with `status: active` and `policy_kind: approved`. For internal
catalogs, use user-selected existing documents, not this catalog's schema.

Edit bundled rules and module introductions in `policy/publication-catalog.json`, then run
`npm run catalog:generate` from the repository root. Generated YAML views are not
independently editable policy. `npm run catalog:check` rejects stale views.

Catalog identity: `azd-publication@5`. See [policy sources and interpretation](policy-sources.md) for the pinned upstream revisions, source-to-rule mapping, local evidence safeguards, and conflict decisions. Upstream requirements inform this catalog; catalog approval is not official azd certification or collection acceptance.

## Active modules

- [Policy profiles](policy-profiles.md) — core, public preparation/submission, and organization selection.
- [Organization requirements](organization-policy.md) — inspecting selected existing documents without a new format.
- [Core evaluation terms](core-evaluation-terms.md) — shared evidence and uncertainty terms for core rules.
- [Core template rules](core-template-rules.md) — root configuration and schema requirements.
- [Core infrastructure rules](core-infrastructure-rules.md) — scenario assets and documented setup paths.
- [Core verification rules](core-verification-rules.md) — execution and teardown evidence.
- [Awesome AZD evaluation terms](awesome-azd-rules.md) — shared definitions for collection rules.
- [Awesome AZD publication rules](awesome-azd-publication-rules.md) — repository publication requirements.
- [Awesome AZD governance rules](awesome-azd-governance-rules.md) — required OSS and governance files.
- [Awesome AZD discoverability rules](awesome-azd-discoverability-rules.md) — repository description and topics.
- [Awesome AZD validation rules](awesome-azd-validation-rules.md) — reviewable validation evidence.
- [Awesome AZD metadata rules](awesome-azd-metadata-rules.md) — path-appropriate gallery metadata.
- [Awesome AZD submission process rules](awesome-azd-submission-process-rules.md) — authorized submission path.
- [Awesome AZD heading rules](awesome-azd-headings-rules.md) — required README headings.
- [Awesome AZD security rules](awesome-azd-security-rules.md) — security validation result.
- [Policy sources and interpretation](policy-sources.md) — provenance and non-enforcing recommendations.
- [Catalog rule schema](catalog-schema.md) — required fields and catalog structure.
- [Catalog runtime ownership](rule-runtime.md) — profile selection, reports, and execution payload.

Only active approved requirements are enforceable. MUST requirements are
enforced; SHOULD and MAY guidance is not. Optional assets—including dev
containers, CI/CD workflows, test suites, screenshots, and videos—are not
failures unless a selected rule requires them. See the [rule schema](catalog-schema.md)
and [runtime ownership](rule-runtime.md) for details.
