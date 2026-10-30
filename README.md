# juphc-tc_pipeline

Tekton CI/CD Pipeline for the Tax Calculator application on IBM Cloud.

## Pipeline Manifests

| File | Description |
| :--- | :--- |
| `tasks.yaml` | The two new Tekton task definitions: `npminstall` (npm ci) and `tests` (Jasmine unit tests) |
| `pipeline.yaml` | Tekton Pipeline definition with steps `clone-source` -> `npminstall` -> `tests` -> `build` -> `deploy` |
| `run.yaml` | PipelineRun manifest with apiVersion, kind, spec, params, and workspaces |

## Resources
All resources use `tekton.dev/v1` and are validated against Tekton Pipeline CRD specifications.
