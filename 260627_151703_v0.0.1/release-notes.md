# Bosgenesis Mop Creation Agent Release Notes

## Document Control

- Release: v0.0.1
- Repository: https://github.com/aveeshek/bosgenesis-mop-creation-agent
- Generated At: 2026-06-27T19:13:50.984100+00:00
- Job ID: scan_b6d73865f4814b3dae6b8f28fd9678b5

## Executive Summary

`bosgenesis-mop-creation-agent` is a spec-first, LLM-assisted agent for reconstructing how a single BOS Genesis Kubernetes namespace was installed and generating reproducible installation documentation. Intent source: `stated`. Evidence: `ev_784bcd339ec39a4de542`.

## Release Overview

Analytics bundle generated for repository review. Missing evidence: Missing HLD documentation.; Missing LLD documentation.; No ADR documentation detected.; No coverage report evidence detected.; No module-level specs.md documentation detected.; No pytest or JUnit test report evidence detected.; Unsupported source extension for structure parsing: .sh

## Repository Overview

Section `inventory` is available with 200 evidence references.

## Project Intent

`bosgenesis-mop-creation-agent` is a spec-first, LLM-assisted agent for reconstructing how a single BOS Genesis Kubernetes namespace was installed and generating reproducible installation documentation. Intent source: `stated`. Evidence: `ev_784bcd339ec39a4de542`.

## Technology Inventory

| Technology | Category | Confidence | Evidence |
| --- | --- | ---: | --- |
| GitHub Actions | ci | 0.95 | `ev_b6086acea1efeb5ef57e`, `ev_2fe6483b679c3d0eee1a` |
| Docker | container | 0.95 | `ev_901a3e8f90aaf0db2251` |
| Helm | deployment | 0.95 | `ev_6c3070e694d7a0cbe2c6` |
| Kubernetes | deployment | 0.90 | `ev_8f611a615db80afd0300`, `ev_080569528f836580f2de`, `ev_f2994c4d1447ab09f328` |
| FastAPI | framework | 0.95 | `ev_ec30f4346576227f0811` |
| MCP | framework | 0.90 | `ev_ec30f4346576227f0811` |
| Pydantic | framework | 0.95 | `ev_ec30f4346576227f0811` |
| Python | language | 0.95 | `ev_188f1f63248192013cef`, `ev_f20ea1a560613cd3ab05`, `ev_49d1302acbb72f60b55a` |
| Shell | language | 0.95 | `ev_d87951ae1935c8fa6e4a`, `ev_d29aab70b93c5cb45015`, `ev_4f15b0bddbdcee98d9d9` |
| Ruff | linting | 0.95 | `ev_ec30f4346576227f0811` |
| Python packaging | packaging | 0.95 | `ev_ec30f4346576227f0811` |
| pytest | testing | 0.95 | `ev_ec30f4346576227f0811` |

## Architecture Overview

### Repository Analysis Flow

Repository evidence is collected before analytics and report rendering. Confidence: `0.95`.

```mermaid
flowchart LR
  repo[GitHub Repository]
  fetch[Repository Fetcher]
  inventory[Inventory Analyzer]
  evidence[Evidence Index]
  analyzers[Analyzer Suite]
  analytics[Analytics Bundle]
  report[Release Note]
  repo --> fetch --> inventory --> evidence --> analyzers --> analytics --> report
```

### C4 Context

High-level context for repository scanning and release-note production. Confidence: `0.80`.

```mermaid
flowchart TB
  user[Reviewer]
  repo[repo]
  agent[BOS Genesis Release Note Agent]
  artifacts[Markdown / HTML / PDF Artifacts]
  user -->|provides GitHub URL| agent
  agent -->|reads public code and metadata| repo
  agent -->|generates| artifacts
  user -->|reviews| artifacts
```

### C4 Container

Runtime containers and their main data flows. Confidence: `0.75`.

```mermaid
flowchart TB
  api[REST API]
  mcp[MCP Server]
  worker[Analyzer Worker]
  storage[(Local Job and Artifact Store)]
  github[Public GitHub Repository]
  api --> storage
  mcp --> storage
  api --> worker
  mcp --> worker
  worker --> github
  worker --> storage
```

### Component Analysis

Analyzer components feeding the normalized analytics bundle. Confidence: `0.85`.

```mermaid
flowchart LR
  evidence[Evidence Index]
  bundle[Analytics Bundle]
  inventory[Inventory]
  evidence --> inventory --> bundle
  technology[Technology]
  evidence --> technology --> bundle
  documentation[Documentation]
  evidence --> documentation --> bundle
  commits[Commits]
  evidence --> commits --> bundle
  code_structure[Code Structure]
  evidence --> code_structure --> bundle
  interfaces[Interfaces]
  evidence --> interfaces --> bundle
  test_coverage[Test Coverage]
  evidence --> test_coverage --> bundle
```

### Deployment Topology

Deployment topology derived only from detected deployment evidence. Confidence: `0.80`.

```mermaid
flowchart TB
  repo[Repository]
  ci[CI/CD]
  repo --> ci
  image[Docker Image]
  ci --> image
  chart[Helm Chart]
  image --> chart
  cluster[Kubernetes Cluster]
  chart --> cluster
```


## Interface Inventory

Detected interfaces: 143.
Recommendations: No explicit CLI command contracts detected.; No explicit MCP tool contracts detected.

## Code Analytics

Section data is available with gaps. Missing evidence: Unsupported source extension for structure parsing: .sh

## Test Analytics

Test source files: 18. Parsed test reports: 0.

## Coverage Analytics

Coverage evidence is missing; no coverage percentage is reported.

## Commit Analytics

Commits analyzed: 21. Authors: 2. Changed files: 201.

## Quality and Risk Assessment

Risky areas: docs/01_SPEC_MOP_CREATION_AGENT.md, src/bosgenesis_mop_creation_agent/rendering/artifact_writer.py, src/bosgenesis_mop_creation_agent/core/orchestrator.py, docs/05_OUTPUT_CONTRACTS.md, docs/SPEC.md, charts/bosgenesis-mop-creation-agent/values.yaml, docs/04_ALGORITHM_MOP_CREATION_AGENT.md, src/bosgenesis_mop_creation_agent/api/routes.py, tests/test_phase1_contract.py, src/bosgenesis_mop_creation_agent/config/settings.py

## Known Gaps

- Missing HLD documentation.
- Missing LLD documentation.
- No ADR documentation detected.
- No coverage report evidence detected.
- No module-level specs.md documentation detected.
- No pytest or JUnit test report evidence detected.
- Unsupported source extension for structure parsing: .sh

## Evidence Traceability

| Evidence ID | Source | Summary |
| --- | --- | --- |
| `ev_0052151b5e12085aa258` | src/bosgenesis_mop_creation_agent/classification/SPEC.md | docs file src/bosgenesis_mop_creation_agent/classification/SPEC.md (2676 bytes) |
| `ev_0268ef00d0b3f78fc84b` | src/bosgenesis_mop_creation_agent/llm/repair_suggester.py | source file src/bosgenesis_mop_creation_agent/llm/repair_suggester.py (11083 bytes) |
| `ev_0426130389f4d0aacd78` | tests/test_phase6_reconstruction.py | test file tests/test_phase6_reconstruction.py (14039 bytes) |
| `ev_0600ed6d76975e46309d` | src/bosgenesis_mop_creation_agent/classification/__init__.py | source file src/bosgenesis_mop_creation_agent/classification/__init__.py (357 bytes) |
| `ev_071dd68631972175d22f` | config/SPEC.md | docs file config/SPEC.md (572 bytes) |
| `ev_077a9f07d4d4e3d0d8ca` | src/bosgenesis_mop_creation_agent/common/SPEC.md | docs file src/bosgenesis_mop_creation_agent/common/SPEC.md (714 bytes) |
| `ev_07863b09db4c80034aa5` | PROJECT_STRUCTURE.md | docs file PROJECT_STRUCTURE.md (1340 bytes) |
| `ev_080569528f836580f2de` | charts/bosgenesis-mop-creation-agent/templates/ingress.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/ingress.yaml (991 bytes) |
| `ev_08d654cf8ab52e33f6f6` | src/bosgenesis_mop_creation_agent/api/SPEC.md | docs file src/bosgenesis_mop_creation_agent/api/SPEC.md (5261 bytes) |
| `ev_0baa91fababa31cf2e8b` | playbook/SPEC.md | docs file playbook/SPEC.md (220 bytes) |
| `ev_0ce98553f4a554d64679` | artifacts/SPEC.md | docs file artifacts/SPEC.md (449 bytes) |
| `ev_0cfd03f419df3f97a5c2` | charts/bosgenesis-mop-creation-agent/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/SPEC.md (363 bytes) |
| `ev_0d2d520f4802afb65d0a` | .agents/skills/SKILL.md | docs file .agents/skills/SKILL.md (8207 bytes) |
| `ev_1089d33f10f8a6fc3202` | docs/kubernetes-mop-sample.md | docs file docs/kubernetes-mop-sample.md (9285 bytes) |
| `ev_1662c963f3d60ebd023d` | src/bosgenesis_mop_creation_agent/evidence/SPEC.md | docs file src/bosgenesis_mop_creation_agent/evidence/SPEC.md (1421 bytes) |
| `ev_188f1f63248192013cef` | src/bosgenesis_mop_creation_agent/__init__.py | source file src/bosgenesis_mop_creation_agent/__init__.py (62 bytes) |
| `ev_18cf9a3425e290665102` | memory/postgresql/SPEC.md | docs file memory/postgresql/SPEC.md (477 bytes) |
| `ev_19f0943d047c77f2add9` | config/settings.yaml | config file config/settings.yaml (2375 bytes) |
| `ev_1ab3c0e6e71d8548f0f0` | src/bosgenesis_mop_creation_agent/config/SPEC.md | docs file src/bosgenesis_mop_creation_agent/config/SPEC.md (4578 bytes) |
| `ev_1ab481bc0908d6697cc7` | src/bosgenesis_mop_creation_agent/reconstruction/helm_hints.py | source file src/bosgenesis_mop_creation_agent/reconstruction/helm_hints.py (3064 bytes) |
| `ev_1bd84fd91f82b3d653d6` | tests/test_phase9_qdrant_references.py | test file tests/test_phase9_qdrant_references.py (9989 bytes) |
| `ev_1c2f5f91625fa7f1f778` | src/bosgenesis_mop_creation_agent/sources/snapshot_models.py | source file src/bosgenesis_mop_creation_agent/sources/snapshot_models.py (1811 bytes) |
| `ev_1cdd1e60c1a9aeae5588` | tests/test_phase1_contract.py | test file tests/test_phase1_contract.py (15627 bytes) |
| `ev_1d90d02bbe80f7957409` | charts/bosgenesis-mop-creation-agent/templates/secret.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/secret.yaml (560 bytes) |
| `ev_1e4e1c4734b674670fe5` | src/bosgenesis_mop_creation_agent/core/orchestrator.py | source file src/bosgenesis_mop_creation_agent/core/orchestrator.py (36273 bytes) |
| `ev_204bd7f6231e70f87416` | knowledge-base/schemas/SPEC.md | docs file knowledge-base/schemas/SPEC.md (196 bytes) |
| `ev_209b5f6df212d83380f7` | src/bosgenesis_mop_creation_agent/retrieval/SPEC.md | docs file src/bosgenesis_mop_creation_agent/retrieval/SPEC.md (1991 bytes) |
| `ev_22a6ed4ca7f3adbfae2c` | deploy/k8s/base/SPEC.md | deployment file deploy/k8s/base/SPEC.md (196 bytes) |
| `ev_23d76f1ffce6a88c1d69` | evaluations/safety/SPEC.md | docs file evaluations/safety/SPEC.md (161 bytes) |
| `ev_23f5748979e6b700c1ca` | docs/06_APPLICATION_MODE.md | docs file docs/06_APPLICATION_MODE.md (7498 bytes) |
| `ev_24117bc58fecd8430636` | src/bosgenesis_mop_creation_agent/memory/models.py | source file src/bosgenesis_mop_creation_agent/memory/models.py (1367 bytes) |
| `ev_26e23036bd3aaaea5648` | src/bosgenesis_mop_creation_agent/models/responses.py | source file src/bosgenesis_mop_creation_agent/models/responses.py (2024 bytes) |
| `ev_2a6862218ee75791692a` | certs/.gitkeep | other file certs/.gitkeep (1 bytes) |
| `ev_2d565ff4b30cd08e0e35` | src/bosgenesis_mop_creation_agent/memory/__init__.py | source file src/bosgenesis_mop_creation_agent/memory/__init__.py (267 bytes) |
| `ev_2defab49cec4132c1a18` | tests/test_artifact_writer_inventory.py | test file tests/test_artifact_writer_inventory.py (29274 bytes) |
| `ev_2fd1feeaf0447d1316a9` | deploy/k8s/SPEC.md | deployment file deploy/k8s/SPEC.md (219 bytes) |
| `ev_2fe6483b679c3d0eee1a` | .github/workflows/ci.yml | ci file .github/workflows/ci.yml (1079 bytes) |
| `ev_3105396696b38db042bc` | docs/DEPLOYMENT.md | docs file docs/DEPLOYMENT.md (3993 bytes) |
| `ev_31d22bb87ee1bae2311e` | src/bosgenesis_mop_creation_agent/mcp_clients/base.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/base.py (8295 bytes) |
| `ev_323a5329d0caebf27b10` | tests/test_phase11_memory_layer.py | test file tests/test_phase11_memory_layer.py (7555 bytes) |
| `ev_32c1c9679f073de29886` | src/SPEC.md | docs file src/SPEC.md (2511 bytes) |
| `ev_33366c91a95b94a95ca1` | src/bosgenesis_mop_creation_agent/core/__init__.py | source file src/bosgenesis_mop_creation_agent/core/__init__.py (35 bytes) |
| `ev_351ded425fdd78780ada` | src/bosgenesis_mop_creation_agent/llm/models.py | source file src/bosgenesis_mop_creation_agent/llm/models.py (3526 bytes) |
| `ev_35cf13e21b009035f3db` | playbook/operations/SPEC.md | docs file playbook/operations/SPEC.md (259 bytes) |
| `ev_3625d4555a5c8e282fa6` | src/bosgenesis_mop_creation_agent/retrieval/qdrant_client.py | source file src/bosgenesis_mop_creation_agent/retrieval/qdrant_client.py (4764 bytes) |
| `ev_3a359b24505fd582a59f` | src/bosgenesis_mop_creation_agent/reconstruction/SPEC.md | docs file src/bosgenesis_mop_creation_agent/reconstruction/SPEC.md (1637 bytes) |
| `ev_3a7a9157b56a4d5222ff` | src/bosgenesis_mop_creation_agent/api/routes.py | source file src/bosgenesis_mop_creation_agent/api/routes.py (13892 bytes) |
| `ev_3c4b17539ba9cd2c957f` | docs/RELEASE_CANDIDATE_RUNBOOK.md | docs file docs/RELEASE_CANDIDATE_RUNBOOK.md (7686 bytes) |
| `ev_3d2320fd55836fa05f41` | evaluations/SPEC.md | docs file evaluations/SPEC.md (303 bytes) |
| `ev_4036b33b55862bade6b0` | docs/03_LLD_MOP_CREATION_AGENT.md | docs file docs/03_LLD_MOP_CREATION_AGENT.md (23592 bytes) |
| `ev_40ee17e1e86637e5691d` | memory/SPEC.md | docs file memory/SPEC.md (631 bytes) |
| `ev_425fe81a2288ad60ba5e` | charts/bosgenesis-mop-creation-agent/templates/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/templates/SPEC.md (218 bytes) |
| `ev_43194ea4572f975ba7e2` | deploy/SPEC.md | deployment file deploy/SPEC.md (199 bytes) |
| `ev_45de8e26b35d0ad2547f` | skills/mop-creation/SPEC.md | docs file skills/mop-creation/SPEC.md (292 bytes) |
| `ev_472f2f5bcb4789336aec` | src/bosgenesis_mop_creation_agent/reconstruction/models.py | source file src/bosgenesis_mop_creation_agent/reconstruction/models.py (1494 bytes) |
| `ev_47a55b015be5c7c9b877` | src/bosgenesis_mop_creation_agent/reconstruction/command_builder.py | source file src/bosgenesis_mop_creation_agent/reconstruction/command_builder.py (2783 bytes) |
| `ev_49d1302acbb72f60b55a` | src/bosgenesis_mop_creation_agent/api/__init__.py | source file src/bosgenesis_mop_creation_agent/api/__init__.py (25 bytes) |
| `ev_49f679337a2007a8f9e5` | src/bosgenesis_mop_creation_agent/security/SPEC.md | docs file src/bosgenesis_mop_creation_agent/security/SPEC.md (1567 bytes) |
| `ev_4b0761b9b085017889ce` | src/bosgenesis_mop_creation_agent/entrypoints/SPEC.md | docs file src/bosgenesis_mop_creation_agent/entrypoints/SPEC.md (960 bytes) |
| `ev_4ddf60a6253d6652e61e` | docs/SAMPLE_REQUESTS.md | docs file docs/SAMPLE_REQUESTS.md (5143 bytes) |
| `ev_4ea23b78fadc76b6f1c8` | knowledge-base/design/SPEC.md | docs file knowledge-base/design/SPEC.md (104 bytes) |
| `ev_4f15b0bddbdcee98d9d9` | playbook/uninstaller.sh | source file playbook/uninstaller.sh (3091 bytes) |
| `ev_4f4a1ac64636e19d0092` | memory/mongodb/SPEC.md | docs file memory/mongodb/SPEC.md (277 bytes) |
| `ev_4fdc15181faf64dc392f` | src/bosgenesis_mop_creation_agent/reconstruction/helm_values.py | source file src/bosgenesis_mop_creation_agent/reconstruction/helm_values.py (2361 bytes) |
| `ev_50874f584ece2a88c538` | codex/SPEC.md | docs file codex/SPEC.md (474 bytes) |
| `ev_5152219a6b59ac74e3f9` | docs/04_ALGORITHM_MOP_CREATION_AGENT.md | docs file docs/04_ALGORITHM_MOP_CREATION_AGENT.md (28900 bytes) |
| `ev_5187ae36c871f2a962be` | evaluations/grounding/SPEC.md | docs file evaluations/grounding/SPEC.md (161 bytes) |
| `ev_5222678b89b2017f2c9b` | docs/07_SAMPLE_MOP_TEMPLATE.md | docs file docs/07_SAMPLE_MOP_TEMPLATE.md (3754 bytes) |
| `ev_535961a4de6d42b11496` | .agents/skills/SPEC.md | docs file .agents/skills/SPEC.md (265 bytes) |
| `ev_537b41a49d80a94a02e4` | tests/test_phase13_observability.py | test file tests/test_phase13_observability.py (6492 bytes) |
| `ev_54e5aa57dfaf97dc61e1` | knowledge-base/interfaces/SPEC.md | docs file knowledge-base/interfaces/SPEC.md (252 bytes) |
| `ev_58b0ba454d3fe1d774c1` | src/bosgenesis_mop_creation_agent/rendering/pdf_renderer.py | source file src/bosgenesis_mop_creation_agent/rendering/pdf_renderer.py (39550 bytes) |
| `ev_59592bf4d8603b0c3b48` | src/bosgenesis_mop_creation_agent/memory/adapters.py | source file src/bosgenesis_mop_creation_agent/memory/adapters.py (12648 bytes) |
| `ev_5969eee61170facc2105` | artifacts/human-mop/human_mop_pdf_template.md | docs file artifacts/human-mop/human_mop_pdf_template.md (11469 bytes) |
| `ev_5ac192b6c38bc9f76279` | codex/config/SPEC.md | docs file codex/config/SPEC.md (186 bytes) |
| `ev_5d3bcf199598ad75c971` | certs/README.md | docs file certs/README.md (740 bytes) |
| `ev_5ecdb5cc186c2f4ba2f0` | deploy/k8s/overlays/SPEC.md | deployment file deploy/k8s/overlays/SPEC.md (185 bytes) |
| `ev_5f4d0996376ac962dc32` | knowledge-base/decisions/SPEC.md | docs file knowledge-base/decisions/SPEC.md (192 bytes) |
| `ev_60deab477ca0f2f90d36` | docs/01_SPEC_MOP_CREATION_AGENT.md | docs file docs/01_SPEC_MOP_CREATION_AGENT.md (25454 bytes) |
| `ev_6201ae1638354df3ce6a` | src/bosgenesis_mop_creation_agent/observability/__init__.py | source file src/bosgenesis_mop_creation_agent/observability/__init__.py (213 bytes) |
| `ev_635e807355e97026e947` | src/bosgenesis_mop_creation_agent/memory/service.py | source file src/bosgenesis_mop_creation_agent/memory/service.py (8584 bytes) |
| `ev_63b1d511b852aa169db2` | src/bosgenesis_mop_creation_agent/mcp_clients/helm_manager_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/helm_manager_client.py (4107 bytes) |
| `ev_65772b76deecb54e00d9` | src/bosgenesis_mop_creation_agent/classification/models.py | source file src/bosgenesis_mop_creation_agent/classification/models.py (1779 bytes) |
| `ev_66a74100a17577b21924` | src/bosgenesis_mop_creation_agent/models/SPEC.md | docs file src/bosgenesis_mop_creation_agent/models/SPEC.md (2302 bytes) |
| `ev_681224dd4ca29aac7785` | tests/test_phase15_release_candidate.py | test file tests/test_phase15_release_candidate.py (2251 bytes) |
| `ev_69e34c08ae190364e14a` | src/bosgenesis_mop_creation_agent/llm/model_gateway.py | source file src/bosgenesis_mop_creation_agent/llm/model_gateway.py (3217 bytes) |
| `ev_6b2de3cb4d549c514fda` | src/bosgenesis_mop_creation_agent/llm/__init__.py | source file src/bosgenesis_mop_creation_agent/llm/__init__.py (243 bytes) |
| `ev_6c3070e694d7a0cbe2c6` | charts/bosgenesis-mop-creation-agent/Chart.yaml | deployment file charts/bosgenesis-mop-creation-agent/Chart.yaml (149 bytes) |
| `ev_707fbdda3e011de136bd` | src/bosgenesis_mop_creation_agent/observability/SPEC.md | docs file src/bosgenesis_mop_creation_agent/observability/SPEC.md (2536 bytes) |
| `ev_732ddcc97564a0954303` | memory/redis/SPEC.md | docs file memory/redis/SPEC.md (390 bytes) |
| `ev_75e2ff0f75a728e6a0b8` | src/bosgenesis_mop_creation_agent/core/SPEC.md | docs file src/bosgenesis_mop_creation_agent/core/SPEC.md (4204 bytes) |
| `ev_776fd8634ea0437dd6ac` | knowledge-base/SPEC.md | docs file knowledge-base/SPEC.md (262 bytes) |
| `ev_77a46d62e0d953597781` | src/bosgenesis_mop_creation_agent/retrieval/models.py | source file src/bosgenesis_mop_creation_agent/retrieval/models.py (1771 bytes) |
| `ev_784bcd339ec39a4de542` | README.md | docs file README.md (4415 bytes) |
| `ev_78b681e1edb3b4b58cfe` | src/bosgenesis_mop_creation_agent/sources/snapshot_selector.py | source file src/bosgenesis_mop_creation_agent/sources/snapshot_selector.py (3372 bytes) |
| `ev_79917ab68fe3c64468bc` | .gitignore | config file .gitignore (218 bytes) |
| `ev_7bc567ecda851f06167f` | .dockerignore | config file .dockerignore (103 bytes) |
| `ev_7f277d97a6b7b73b927e` | charts/bosgenesis-mop-creation-agent/templates/configmap.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/configmap.yaml (779 bytes) |
| `ev_7f577645775b751d677b` | artifacts/installation-notes/installation_notes_template.md | docs file artifacts/installation-notes/installation_notes_template.md (10092 bytes) |
| `ev_813c33c146f8da3a345c` | samples/requests/SPEC.md | docs file samples/requests/SPEC.md (355 bytes) |
| `ev_831ef514432fb46e6b39` | charts/bosgenesis-mop-creation-agent/templates/pvc.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/pvc.yaml (680 bytes) |
| `ev_8377e9c7cf974a6288aa` | docs/K8S_INSPECTOR_RESOURCE_DETAIL_ENRICHMENT_PLAN.md | docs file docs/K8S_INSPECTOR_RESOURCE_DETAIL_ENRICHMENT_PLAN.md (8029 bytes) |
| `ev_83d9a81bf35eeab55ef1` | src/bosgenesis_mop_creation_agent/reconstruction/planner.py | source file src/bosgenesis_mop_creation_agent/reconstruction/planner.py (11834 bytes) |
| `ev_843094d33be707a9c8d6` | .github/SPEC.md | docs file .github/SPEC.md (272 bytes) |
| `ev_86e912012e520b41cf1e` | TECH_STACK.md | docs file TECH_STACK.md (1192 bytes) |
| `ev_87f5728e02f306e0be56` | src/bosgenesis_mop_creation_agent/retrieval/reference_lookup.py | source file src/bosgenesis_mop_creation_agent/retrieval/reference_lookup.py (12202 bytes) |
| `ev_89d8f11fd5b2aa7b8e06` | src/bosgenesis_mop_creation_agent/reasoning/SPEC.md | docs file src/bosgenesis_mop_creation_agent/reasoning/SPEC.md (2231 bytes) |
| `ev_8b556e29b2d52c75f70a` | tests/SPEC.md | test file tests/SPEC.md (1442 bytes) |
| `ev_8c1ddef981e289ee78a3` | codex/prompts/SPEC.md | docs file codex/prompts/SPEC.md (313 bytes) |
| `ev_8da7de31d192770cf492` | docs/SPEC.md | docs file docs/SPEC.md (3905 bytes) |
| `ev_8e81e3cd124cf792c7bb` | samples/requests/platform-only-generate.json | config file samples/requests/platform-only-generate.json (379 bytes) |
| `ev_8f5a941a994ffc5ac673` | src/bosgenesis_mop_creation_agent/reconstruction/manifest_normalizer.py | source file src/bosgenesis_mop_creation_agent/reconstruction/manifest_normalizer.py (8191 bytes) |
| `ev_8f611a615db80afd0300` | charts/bosgenesis-mop-creation-agent/templates/deployment.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/deployment.yaml (2581 bytes) |
| `ev_901a3e8f90aaf0db2251` | Dockerfile | deployment file Dockerfile (553 bytes) |
| `ev_92ff6998cf2c8e2081a5` | charts/bosgenesis-mop-creation-agent/.helmignore | deployment file charts/bosgenesis-mop-creation-agent/.helmignore (65 bytes) |
| `ev_93b2807fb3eccdf552ac` | docs/05_OUTPUT_CONTRACTS.md | docs file docs/05_OUTPUT_CONTRACTS.md (18495 bytes) |
| `ev_93cfe9181c773def1c26` | src/bosgenesis_mop_creation_agent/entrypoints/main.py | source file src/bosgenesis_mop_creation_agent/entrypoints/main.py (311 bytes) |
| `ev_963e05b2097802f6492a` | AGENTS.md | docs file AGENTS.md (1880 bytes) |
| `ev_9b1d206994d0c4741e43` | samples/requests/application-mode-smoke-generate.json | config file samples/requests/application-mode-smoke-generate.json (388 bytes) |
| `ev_9bdb461f26af1745d311` | docs/CREDENTIALS.md | docs file docs/CREDENTIALS.md (13166 bytes) |
| `ev_9f5d412c3b8a17da11e5` | samples/SPEC.md | docs file samples/SPEC.md (431 bytes) |
| `ev_9fdaa8164931276f96a7` | charts/bosgenesis-mop-creation-agent/values.credentials.example.yaml | deployment file charts/bosgenesis-mop-creation-agent/values.credentials.example.yaml (596 bytes) |
| `ev_9fe451c9946826eba016` | memory/clickhouse/SPEC.md | docs file memory/clickhouse/SPEC.md (318 bytes) |
| `ev_a11d3e77680922020905` | reports/SPEC.md | docs file reports/SPEC.md (901 bytes) |
| `ev_a11f9d98cfc000e33443` | src/bosgenesis_mop_creation_agent/api/mcp.py | source file src/bosgenesis_mop_creation_agent/api/mcp.py (7200 bytes) |
| `ev_a1af6972dc8cb9e5401d` | src/bosgenesis_mop_creation_agent/memory/SPEC.md | docs file src/bosgenesis_mop_creation_agent/memory/SPEC.md (3714 bytes) |
| `ev_a2497a189af5f9bd0cc3` | src/bosgenesis_mop_creation_agent/observability/service.py | source file src/bosgenesis_mop_creation_agent/observability/service.py (17472 bytes) |
| `ev_a588cd793317376b1b22` | src/bosgenesis_mop_creation_agent/validation/SPEC.md | docs file src/bosgenesis_mop_creation_agent/validation/SPEC.md (1964 bytes) |
| `ev_a77917e72b9b76b297c2` | memory/langmem/SPEC.md | docs file memory/langmem/SPEC.md (275 bytes) |
| `ev_aab9a060d9ddd7d708c3` | tests/test_phase7_pdf_renderer.py | test file tests/test_phase7_pdf_renderer.py (8692 bytes) |
| `ev_aaba0018cf37b7ff1381` | playbook/rollback/SPEC.md | docs file playbook/rollback/SPEC.md (224 bytes) |
| `ev_aafcea1494a97a48f6da` | src/bosgenesis_mop_creation_agent/mcp_clients/enrichment.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/enrichment.py (9463 bytes) |
| `ev_ad0c06e792966a329074` | tests/test_health.py | test file tests/test_health.py (1746 bytes) |
| `ev_ad8f40f472dbb94150ed` | charts/SPEC.md | deployment file charts/SPEC.md (228 bytes) |
| `ev_aee062aa5d7fde8e1eed` | src/bosgenesis_mop_creation_agent/langchain/SPEC.md | docs file src/bosgenesis_mop_creation_agent/langchain/SPEC.md (1133 bytes) |
| `ev_b13287a515459389d159` | docs/02_HLD_MOP_CREATION_AGENT.md | docs file docs/02_HLD_MOP_CREATION_AGENT.md (14244 bytes) |
| `ev_b24751f49c2614350135` | src/bosgenesis_mop_creation_agent/config/settings.py | source file src/bosgenesis_mop_creation_agent/config/settings.py (15051 bytes) |
| `ev_b2578dc17cc6380ab609` | charts/bosgenesis-mop-creation-agent/values.yaml | deployment file charts/bosgenesis-mop-creation-agent/values.yaml (5875 bytes) |
| `ev_b3b68b37cb6bf895acb1` | src/bosgenesis_mop_creation_agent/llm/bounded_reasoning.py | source file src/bosgenesis_mop_creation_agent/llm/bounded_reasoning.py (15011 bytes) |
| `ev_b3c8afcc9fd21a2007b5` | tests/e2e/SPEC.md | test file tests/e2e/SPEC.md (294 bytes) |
| `ev_b5d280e9c5caed320e66` | artifacts/installation-notes/SPEC.md | docs file artifacts/installation-notes/SPEC.md (1174 bytes) |
| `ev_b6086acea1efeb5ef57e` | .github/workflows/SPEC.md | ci file .github/workflows/SPEC.md (574 bytes) |
| `ev_b638899422695f552e63` | src/bosgenesis_mop_creation_agent/config/__init__.py | source file src/bosgenesis_mop_creation_agent/config/__init__.py (38 bytes) |
| `ev_b6aac2c4e6a1e70406be` | charts/bosgenesis-mop-creation-agent/values/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/values/SPEC.md (310 bytes) |
| `ev_b6be84dc55db09360c62` | codex/config/config.toml | config file codex/config/config.toml (937 bytes) |
| `ev_b8567446c169ff854087` | codex/skills/SPEC.md | docs file codex/skills/SPEC.md (221 bytes) |
| `ev_b96eed54e2c70b0cfaab` | playbook/validation/SPEC.md | docs file playbook/validation/SPEC.md (300 bytes) |
| `ev_b9f026a2c436932aa44a` | src/bosgenesis_mop_creation_agent/models/requests.py | source file src/bosgenesis_mop_creation_agent/models/requests.py (2539 bytes) |
| `ev_bb5b1a01b00d13daf967` | src/bosgenesis_mop_creation_agent/SPEC.md | docs file src/bosgenesis_mop_creation_agent/SPEC.md (2009 bytes) |
| `ev_bd4111b36edaf96dd28d` | src/bosgenesis_mop_creation_agent/retrieval/component_query_builder.py | source file src/bosgenesis_mop_creation_agent/retrieval/component_query_builder.py (5788 bytes) |
| `ev_bd6589d7eb3e36aa08ed` | tests/test_phase10_bounded_reasoning.py | test file tests/test_phase10_bounded_reasoning.py (9367 bytes) |
| `ev_c0faf9dead52752d1d85` | .agents/skills/SKILLS.md | docs file .agents/skills/SKILLS.md (9902 bytes) |
| `ev_c1fead4531e5a980efb5` | src/bosgenesis_mop_creation_agent/documents/SPEC.md | docs file src/bosgenesis_mop_creation_agent/documents/SPEC.md (2776 bytes) |
| `ev_c3c4a84d699aa057bac7` | docs/CONTEXT_SNAPSHOT.md | docs file docs/CONTEXT_SNAPSHOT.md (7259 bytes) |
| `ev_c40a78e6528090e2dda2` | skills/SPEC.md | docs file skills/SPEC.md (243 bytes) |
| `ev_c48f4dfdee2b10227748` | src/bosgenesis_mop_creation_agent/common/logging.py | source file src/bosgenesis_mop_creation_agent/common/logging.py (1803 bytes) |
| `ev_c4a55394f862bd3a26e2` | tests/test_phase62_llm_repair.py | test file tests/test_phase62_llm_repair.py (9549 bytes) |
| `ev_c6511f6183395609dc05` | artifacts/human-mop/professional_mop_pdf_template.yaml | config file artifacts/human-mop/professional_mop_pdf_template.yaml (1794 bytes) |
| `ev_c7070f25eda8ec86c932` | playbook/test-report.ps1 | other file playbook/test-report.ps1 (958 bytes) |
| `ev_c7a2370e16068b1f56dd` | tests/test_phase5_classification.py | test file tests/test_phase5_classification.py (6655 bytes) |
| `ev_c80bdb153028a01186fa` | src/bosgenesis_mop_creation_agent/sources/clickhouse_snapshot_reader.py | source file src/bosgenesis_mop_creation_agent/sources/clickhouse_snapshot_reader.py (6669 bytes) |
| `ev_ca8f988bf0ee6fa7da0b` | src/bosgenesis_mop_creation_agent/classification/resource_classifier.py | source file src/bosgenesis_mop_creation_agent/classification/resource_classifier.py (9076 bytes) |
| `ev_cd8705cceb6993043643` | src/bosgenesis_mop_creation_agent/api/app.py | source file src/bosgenesis_mop_creation_agent/api/app.py (1172 bytes) |
| `ev_cdf98740f776746aa8b8` | tests/contracts/SPEC.md | test file tests/contracts/SPEC.md (273 bytes) |
| `ev_d169351b3d3afbec5260` | src/bosgenesis_mop_creation_agent/langgraph/SPEC.md | docs file src/bosgenesis_mop_creation_agent/langgraph/SPEC.md (1505 bytes) |
| `ev_d29aab70b93c5cb45015` | playbook/test-report.sh | source file playbook/test-report.sh (761 bytes) |
| `ev_d4aeb8ff586d14d935e1` | src/bosgenesis_mop_creation_agent/sources/SPEC.md | docs file src/bosgenesis_mop_creation_agent/sources/SPEC.md (1073 bytes) |
| `ev_d6af70821f6ace6df788` | tests/test_phase4_mcp_enrichment.py | test file tests/test_phase4_mcp_enrichment.py (10444 bytes) |
| `ev_d74dca40437c40bf6ace` | codex/skills/SKILL.md | docs file codex/skills/SKILL.md (2712 bytes) |
| `ev_d87951ae1935c8fa6e4a` | playbook/deploy.sh | source file playbook/deploy.sh (8003 bytes) |
| `ev_d94e978aedda0ced089b` | src/bosgenesis_mop_creation_agent/persistence/SPEC.md | docs file src/bosgenesis_mop_creation_agent/persistence/SPEC.md (1919 bytes) |
| `ev_d97eb06e292203c63406` | src/bosgenesis_mop_creation_agent/retrieval/__init__.py | source file src/bosgenesis_mop_creation_agent/retrieval/__init__.py (258 bytes) |
| `ev_da1bcdbc5d75fa7c17c2` | certs/SPEC.md | docs file certs/SPEC.md (1369 bytes) |
| `ev_db883cb6662b135c6ce4` | playbook/deployment/SPEC.md | docs file playbook/deployment/SPEC.md (303 bytes) |
| `ev_dba91b6f03ea7cb64899` | src/bosgenesis_mop_creation_agent/collectors/SPEC.md | docs file src/bosgenesis_mop_creation_agent/collectors/SPEC.md (1181 bytes) |
| `ev_dbb943129126628d5776` | src/bosgenesis_mop_creation_agent/models/__init__.py | source file src/bosgenesis_mop_creation_agent/models/__init__.py (37 bytes) |
| `ev_e147960401a8293a097c` | src/bosgenesis_mop_creation_agent/application/SPEC.md | docs file src/bosgenesis_mop_creation_agent/application/SPEC.md (1429 bytes) |
| `ev_e2988186b47bc2e12e42` | src/bosgenesis_mop_creation_agent/entrypoints/__init__.py | source file src/bosgenesis_mop_creation_agent/entrypoints/__init__.py (28 bytes) |
| `ev_e2d1523744154f31e828` | src/bosgenesis_mop_creation_agent/mcp_clients/data_ingestion_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/data_ingestion_client.py (1995 bytes) |
| `ev_e74a9740d2db995eaa9b` | tests/test_snapshot_selector.py | test file tests/test_snapshot_selector.py (3163 bytes) |
| `ev_e7d05bb30e5b7c6bb6cc` | reports/.gitkeep | other file reports/.gitkeep (1 bytes) |
| `ev_ea00b02c4f9ffcc23fce` | src/bosgenesis_mop_creation_agent/reconstruction/__init__.py | source file src/bosgenesis_mop_creation_agent/reconstruction/__init__.py (132 bytes) |
| `ev_ec30f4346576227f0811` | pyproject.toml | config file pyproject.toml (1409 bytes) |
| `ev_ee60d0ddf3ee67fa9148` | LICENSE | other file LICENSE (2417 bytes) |
| `ev_f059dcdc5cb985152c02` | SPEC.md | docs file SPEC.md (1808 bytes) |
| `ev_f0c67287b563fc5ce61c` | src/bosgenesis_mop_creation_agent/reconstruction/quality_gate.py | source file src/bosgenesis_mop_creation_agent/reconstruction/quality_gate.py (2454 bytes) |
| `ev_f170d111816a9d0d5365` | src/bosgenesis_mop_creation_agent/mcp_clients/k8s_inspector_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/k8s_inspector_client.py (7628 bytes) |
| `ev_f1e00e3f33471b21c765` | artifacts/human-mop/SPEC.md | docs file artifacts/human-mop/SPEC.md (2238 bytes) |
| `ev_f1e2bc7dd72c1baaef83` | knowledge-base/session/SPEC.md | docs file knowledge-base/session/SPEC.md (199 bytes) |
| `ev_f20ea1a560613cd3ab05` | src/bosgenesis_mop_creation_agent/__main__.py | source file src/bosgenesis_mop_creation_agent/__main__.py (105 bytes) |
| `ev_f2994c4d1447ab09f328` | charts/bosgenesis-mop-creation-agent/templates/service.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/service.yaml (428 bytes) |
| `ev_f2e79cdfa111f615987d` | charts/bosgenesis-mop-creation-agent/templates/_helpers.tpl | deployment file charts/bosgenesis-mop-creation-agent/templates/_helpers.tpl (1481 bytes) |
| `ev_f35ab2db1933a6d4e3d6` | src/bosgenesis_mop_creation_agent/rendering/artifact_writer.py | source file src/bosgenesis_mop_creation_agent/rendering/artifact_writer.py (88609 bytes) |
| `ev_f4405de3ace79e3f44b0` | src/bosgenesis_mop_creation_agent/rendering/SPEC.md | docs file src/bosgenesis_mop_creation_agent/rendering/SPEC.md (4875 bytes) |
| `ev_f5d8d8e328821429380f` | src/bosgenesis_mop_creation_agent/sources/postgres_snapshot_reader.py | source file src/bosgenesis_mop_creation_agent/sources/postgres_snapshot_reader.py (7148 bytes) |
| `ev_f91486fe021397fa0c94` | src/bosgenesis_mop_creation_agent/common/__init__.py | source file src/bosgenesis_mop_creation_agent/common/__init__.py (25 bytes) |
| `ev_fa057454d41ad452e9ba` | src/bosgenesis_mop_creation_agent/llm/SPEC.md | docs file src/bosgenesis_mop_creation_agent/llm/SPEC.md (5822 bytes) |
| `ev_fbf6509cc8f9052736bc` | src/bosgenesis_mop_creation_agent/mcp_clients/SPEC.md | docs file src/bosgenesis_mop_creation_agent/mcp_clients/SPEC.md (1594 bytes) |
| `ev_fc3beb93daa4fb4c5410` | tests/fixtures/SPEC.md | test file tests/fixtures/SPEC.md (231 bytes) |
| `ev_fcbe160049fc17fa731c` | src/bosgenesis_mop_creation_agent/observability/models.py | source file src/bosgenesis_mop_creation_agent/observability/models.py (1517 bytes) |

## Appendix

Generated by BOS Genesis Release Note Agent.

## Summary
Release-note-agent document preserved as the primary draft.

## Source Evidence
- GitHub URL: https://github.com/aveeshek/bosgenesis-mop-creation-agent
- release-note-agent status: `success`

## Repository Scan
- Repository: https://github.com/aveeshek/bosgenesis-mop-creation-agent
- Source ref: tag phase16.2-final-clone-reconstruction
- Clone status: `success`
- Primary language: `python`
- Files inspected: 91 code file(s), 2 manifest(s)
- Local checkout cleanup: `removed`

### Vulnerability Matrix
| Category | Severity | Findings | Evidence | Recommendation |
| --- | --- | ---: | --- | --- |
| Cryptography | medium | 2 | src/bosgenesis_mop_creation_agent/reconstruction/planner.py:195 (weak_hash) | Use SHA-256 or stronger algorithms unless this is non-security hashing. |

### Code Quality Matrix
| Area | Tool | Result | Findings | Notes |
| --- | --- | --- | ---: | --- |
| Language mix | repository inventory | python | 91 | Detected 2 dependency/build manifest(s). |
| Code quality | ruff | completed | 0 | pylint was unavailable; ruff was used as fallback. |
| Quality categories | ruff | summarized | 0 | lint: 0 |

### LLM Security Review Summary
- Overall risk: `low`
- Summary: The static repository scan identified a single recurring vulnerability theme: use of a weak cryptographic hash (SHA-1) in the reconstruction planner. No other issues were reported by the linting fallback (ruff), and there were no flagged secrets or manifest dependency findings in the provided output. Given the limited scope and the likely non-security use of the hash (short identifiers derived from names), the current overall risk is low; however, replacing SHA-1 is recommended to reduce collision risk and prevent potential future misuse.
- Safe reasoning summary: Findings are limited to two instances of SHA-1 usage within the same Python module. No additional categories (secrets exposure, injection, insecure deserialization, misconfigurations) were reported in the provided scan results, and dependency information was not analyzed. The risk assessment assumes the hash is used for non-cryptographic identification; if it impacts security decisions (e.g., access control, integrity checks), risk would increase. The absence of broader SAST/SCA and secret-scanning results suggests potential blind spots; therefore, recommendations prioritize cryptographic corrections and improved security tooling coverage.
