# Source Conflicts and Selected Interpretations

| Difference | Catalog decision |
| --- | --- |
| Definition of done says repository root; publishing guidance allows a documented working directory. | Treat the documented or explicitly selected working directory as template root. Resolve it before checking files. Do not fail a monorepo because its repository root has no `azure.yaml`. If unresolved, report uncertainty. |
| Baseline requires `LICENSE.md`, `.github/CODE_OF_CONDUCT.md`, and plural topics `azd-templates` and `ai-azd-templates`; validator defaults may differ. | Apply the pinned profile. Explain validator settings separately; do not silently substitute defaults or claim the differences are settled by collection maintainers. The AI-named topic does not require an AI application. |
| Definition of done requires `Important Security Notice`, but its example `README_H2_TAG` lists only Features, Getting Started, Guidance, and Resources. | Inspect all five headings independently. A run checking only the four example headings cannot establish the full heading rule. |
| Collection automation checks dev containers and workflows by default. | These remain optional. Recommend configuring validation paths and disabling dev-container execution when intentionally omitted; do not create failures for their absence. |

Validator configuration is evidence about which checks ran, not a competing
policy authority. Preserve the selected profile and report unresolved
differences without asserting guaranteed gallery acceptance.
