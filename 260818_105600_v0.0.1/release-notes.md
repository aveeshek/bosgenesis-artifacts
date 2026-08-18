# Bosgenesis Mop Creation Agent Release Notes

## Document Control

- Release: v0.0.1
- Repository: https://github.com/aveeshek/bosgenesis-mop-creation-agent
- Generated At: 2026-08-18T14:53:57.261403+00:00
- Job ID: scan_616a8938704c4122b6ef7713dface36e

## Executive Summary

`bosgenesis-mop-creation-agent` is a spec-first, LLM-assisted agent for reconstructing how a single BOS Genesis Kubernetes namespace was installed and generating reproducible installation documentation. Intent source: `stated`. Evidence: `ev_20a6b7675c509194568e`.

## Release Overview

Analytics bundle generated for repository review. Missing evidence: Missing HLD documentation.; Missing LLD documentation.; No ADR documentation detected.; No coverage report evidence detected.; No module-level specs.md documentation detected.; No pytest or JUnit test report evidence detected.; Unsupported source extension for structure parsing: .sh

## Repository Overview

Section `inventory` is available with 200 evidence references.

## Project Intent

`bosgenesis-mop-creation-agent` is a spec-first, LLM-assisted agent for reconstructing how a single BOS Genesis Kubernetes namespace was installed and generating reproducible installation documentation. Intent source: `stated`. Evidence: `ev_20a6b7675c509194568e`.

## Technology Inventory

| Technology | Category | Confidence | Evidence |
| --- | --- | ---: | --- |
| GitHub Actions | ci | 0.95 | `ev_916e745d563dda1c902b`, `ev_e4932fc2064e8da4f4dc` |
| Docker | container | 0.95 | `ev_201006f8f34aff73a2f4` |
| Helm | deployment | 0.95 | `ev_8a68a6a600c7fd354070` |
| Kubernetes | deployment | 0.90 | `ev_782f3cfd268c1cbf8b7f`, `ev_b4d707d49956529a42ad`, `ev_31fe612f79396dd8d571` |
| FastAPI | framework | 0.95 | `ev_85a0c65e4054357b293a` |
| MCP | framework | 0.90 | `ev_85a0c65e4054357b293a` |
| Pydantic | framework | 0.95 | `ev_85a0c65e4054357b293a` |
| Python | language | 0.95 | `ev_49b1dfb0184ff05ff4c0`, `ev_96cd759cc3bf8cb19af3`, `ev_0cf17f93dd0ba1885497` |
| Shell | language | 0.95 | `ev_aaf91001d9083b18a9d7`, `ev_3295fb1ff1cf08932237`, `ev_faea43427c013b484a72` |
| Ruff | linting | 0.95 | `ev_85a0c65e4054357b293a` |
| Python packaging | packaging | 0.95 | `ev_85a0c65e4054357b293a` |
| pytest | testing | 0.95 | `ev_85a0c65e4054357b293a` |

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
| `ev_0146105832155f4be295` | src/bosgenesis_mop_creation_agent/evidence/SPEC.md | docs file src/bosgenesis_mop_creation_agent/evidence/SPEC.md (1421 bytes) |
| `ev_01eb766cc75cd06890a2` | src/bosgenesis_mop_creation_agent/sources/SPEC.md | docs file src/bosgenesis_mop_creation_agent/sources/SPEC.md (1073 bytes) |
| `ev_022f6c6e150b6ce3d79b` | src/bosgenesis_mop_creation_agent/rendering/SPEC.md | docs file src/bosgenesis_mop_creation_agent/rendering/SPEC.md (4875 bytes) |
| `ev_028cc74fcb753e698ba6` | src/bosgenesis_mop_creation_agent/observability/service.py | source file src/bosgenesis_mop_creation_agent/observability/service.py (17472 bytes) |
| `ev_039d34ea5f40a5f3f7da` | src/bosgenesis_mop_creation_agent/retrieval/__init__.py | source file src/bosgenesis_mop_creation_agent/retrieval/__init__.py (258 bytes) |
| `ev_05a275dce66e58f75d4a` | src/bosgenesis_mop_creation_agent/llm/SPEC.md | docs file src/bosgenesis_mop_creation_agent/llm/SPEC.md (5822 bytes) |
| `ev_0cf17f93dd0ba1885497` | src/bosgenesis_mop_creation_agent/api/__init__.py | source file src/bosgenesis_mop_creation_agent/api/__init__.py (25 bytes) |
| `ev_0f49a571f7e8e79b2070` | tests/SPEC.md | test file tests/SPEC.md (1442 bytes) |
| `ev_1135262a2d379e6748d2` | AGENTS.md | docs file AGENTS.md (1880 bytes) |
| `ev_115a3f7911fab6b08f9a` | config/settings.yaml | config file config/settings.yaml (2375 bytes) |
| `ev_11ec5bcd61ad2ed0e2c1` | src/bosgenesis_mop_creation_agent/llm/bounded_reasoning.py | source file src/bosgenesis_mop_creation_agent/llm/bounded_reasoning.py (15011 bytes) |
| `ev_132c76756412c7513340` | tests/test_phase13_observability.py | test file tests/test_phase13_observability.py (6492 bytes) |
| `ev_13943e0ee15a9e70424c` | src/bosgenesis_mop_creation_agent/common/__init__.py | source file src/bosgenesis_mop_creation_agent/common/__init__.py (25 bytes) |
| `ev_15ff2abb7299d5394420` | skills/SPEC.md | docs file skills/SPEC.md (243 bytes) |
| `ev_16a895c2442dcf955feb` | playbook/operations/SPEC.md | docs file playbook/operations/SPEC.md (259 bytes) |
| `ev_17b7b5b0369c36fcaaf1` | charts/bosgenesis-mop-creation-agent/values.yaml | deployment file charts/bosgenesis-mop-creation-agent/values.yaml (5875 bytes) |
| `ev_17e9ce4bfd9b31a4c957` | evaluations/safety/SPEC.md | docs file evaluations/safety/SPEC.md (161 bytes) |
| `ev_193e7b4378b74d23628a` | tests/test_phase7_pdf_renderer.py | test file tests/test_phase7_pdf_renderer.py (8692 bytes) |
| `ev_194efe7802196d59a379` | src/bosgenesis_mop_creation_agent/api/app.py | source file src/bosgenesis_mop_creation_agent/api/app.py (1172 bytes) |
| `ev_1bad9665507cd9a4e99f` | src/bosgenesis_mop_creation_agent/SPEC.md | docs file src/bosgenesis_mop_creation_agent/SPEC.md (2009 bytes) |
| `ev_1cffc45aaeec82f50504` | src/bosgenesis_mop_creation_agent/classification/models.py | source file src/bosgenesis_mop_creation_agent/classification/models.py (1779 bytes) |
| `ev_1d0c7efd88107d2ee076` | docs/DEPLOYMENT.md | docs file docs/DEPLOYMENT.md (3993 bytes) |
| `ev_1e1457f85d6754df37bc` | docs/05_OUTPUT_CONTRACTS.md | docs file docs/05_OUTPUT_CONTRACTS.md (18495 bytes) |
| `ev_1e9fc0764c03df938b8e` | artifacts/human-mop/human_mop_pdf_template.md | docs file artifacts/human-mop/human_mop_pdf_template.md (11469 bytes) |
| `ev_1f20c82caa8f38e42090` | skills/mop-creation/SPEC.md | docs file skills/mop-creation/SPEC.md (292 bytes) |
| `ev_1f70ed188df9c41ad79c` | src/bosgenesis_mop_creation_agent/documents/SPEC.md | docs file src/bosgenesis_mop_creation_agent/documents/SPEC.md (2776 bytes) |
| `ev_201006f8f34aff73a2f4` | Dockerfile | deployment file Dockerfile (553 bytes) |
| `ev_201ab5309ba694245f0d` | src/bosgenesis_mop_creation_agent/application/SPEC.md | docs file src/bosgenesis_mop_creation_agent/application/SPEC.md (1429 bytes) |
| `ev_203db3664a8c5bbcf37e` | src/bosgenesis_mop_creation_agent/memory/adapters.py | source file src/bosgenesis_mop_creation_agent/memory/adapters.py (12648 bytes) |
| `ev_20a4040834401b04b25d` | tests/fixtures/SPEC.md | test file tests/fixtures/SPEC.md (231 bytes) |
| `ev_20a6b7675c509194568e` | README.md | docs file README.md (4415 bytes) |
| `ev_211ce91d3fc6e0c6f884` | playbook/test-report.ps1 | other file playbook/test-report.ps1 (958 bytes) |
| `ev_2164b3cbcc3f428da7c9` | src/bosgenesis_mop_creation_agent/core/__init__.py | source file src/bosgenesis_mop_creation_agent/core/__init__.py (35 bytes) |
| `ev_22e0347cc8d2a26d5df2` | src/bosgenesis_mop_creation_agent/rendering/artifact_writer.py | source file src/bosgenesis_mop_creation_agent/rendering/artifact_writer.py (88609 bytes) |
| `ev_23cb139a944f4c738f54` | src/bosgenesis_mop_creation_agent/entrypoints/main.py | source file src/bosgenesis_mop_creation_agent/entrypoints/main.py (311 bytes) |
| `ev_241cf4f5a60f905cad17` | src/bosgenesis_mop_creation_agent/reconstruction/command_builder.py | source file src/bosgenesis_mop_creation_agent/reconstruction/command_builder.py (2783 bytes) |
| `ev_25174f58bd60c9a97ddc` | deploy/k8s/base/SPEC.md | deployment file deploy/k8s/base/SPEC.md (196 bytes) |
| `ev_254f9437eb8cf665aa0c` | samples/requests/application-mode-smoke-generate.json | config file samples/requests/application-mode-smoke-generate.json (388 bytes) |
| `ev_25a99a8db88d55cb0a7d` | artifacts/installation-notes/installation_notes_template.md | docs file artifacts/installation-notes/installation_notes_template.md (10092 bytes) |
| `ev_2653254f5aa71aaeef2b` | src/bosgenesis_mop_creation_agent/langgraph/SPEC.md | docs file src/bosgenesis_mop_creation_agent/langgraph/SPEC.md (1505 bytes) |
| `ev_27a1cb9dc07673d332b3` | src/bosgenesis_mop_creation_agent/sources/clickhouse_snapshot_reader.py | source file src/bosgenesis_mop_creation_agent/sources/clickhouse_snapshot_reader.py (6669 bytes) |
| `ev_298cfa71872eda43d664` | src/bosgenesis_mop_creation_agent/security/SPEC.md | docs file src/bosgenesis_mop_creation_agent/security/SPEC.md (1567 bytes) |
| `ev_2bad4a9da92ee8f30d69` | tests/test_phase62_llm_repair.py | test file tests/test_phase62_llm_repair.py (9549 bytes) |
| `ev_2c69daac2c19582f1fe7` | src/bosgenesis_mop_creation_agent/mcp_clients/helm_manager_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/helm_manager_client.py (4107 bytes) |
| `ev_2db9af9a74ee16489643` | src/bosgenesis_mop_creation_agent/llm/models.py | source file src/bosgenesis_mop_creation_agent/llm/models.py (3526 bytes) |
| `ev_2df1822e08182fef0845` | src/bosgenesis_mop_creation_agent/memory/models.py | source file src/bosgenesis_mop_creation_agent/memory/models.py (1367 bytes) |
| `ev_30bba5f12c3ab8546b50` | docs/CREDENTIALS.md | docs file docs/CREDENTIALS.md (13166 bytes) |
| `ev_31fe612f79396dd8d571` | charts/bosgenesis-mop-creation-agent/templates/service.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/service.yaml (428 bytes) |
| `ev_3295fb1ff1cf08932237` | playbook/test-report.sh | source file playbook/test-report.sh (761 bytes) |
| `ev_3352fc52e095f06247f8` | charts/SPEC.md | deployment file charts/SPEC.md (228 bytes) |
| `ev_3510748200e5e9f6c41d` | playbook/rollback/SPEC.md | docs file playbook/rollback/SPEC.md (224 bytes) |
| `ev_354430affbd21392188a` | reports/.gitkeep | other file reports/.gitkeep (1 bytes) |
| `ev_3555cc33edfa634c1ca1` | src/bosgenesis_mop_creation_agent/sources/postgres_snapshot_reader.py | source file src/bosgenesis_mop_creation_agent/sources/postgres_snapshot_reader.py (7148 bytes) |
| `ev_3612903d576703b12734` | src/bosgenesis_mop_creation_agent/mcp_clients/data_ingestion_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/data_ingestion_client.py (1995 bytes) |
| `ev_37d32a6f2a259c152bba` | deploy/SPEC.md | deployment file deploy/SPEC.md (199 bytes) |
| `ev_37d37ea14dba9bcf9529` | src/bosgenesis_mop_creation_agent/langchain/SPEC.md | docs file src/bosgenesis_mop_creation_agent/langchain/SPEC.md (1133 bytes) |
| `ev_39fcda861370f8e46600` | src/bosgenesis_mop_creation_agent/retrieval/qdrant_client.py | source file src/bosgenesis_mop_creation_agent/retrieval/qdrant_client.py (4764 bytes) |
| `ev_3a894335c68cfe984dd1` | src/bosgenesis_mop_creation_agent/reconstruction/SPEC.md | docs file src/bosgenesis_mop_creation_agent/reconstruction/SPEC.md (1637 bytes) |
| `ev_3c09f5c3c47bfd76027e` | src/bosgenesis_mop_creation_agent/classification/SPEC.md | docs file src/bosgenesis_mop_creation_agent/classification/SPEC.md (2676 bytes) |
| `ev_3d4022da0b076ff45c7f` | charts/bosgenesis-mop-creation-agent/templates/_helpers.tpl | deployment file charts/bosgenesis-mop-creation-agent/templates/_helpers.tpl (1481 bytes) |
| `ev_3e4ffcf7e5d99f4b9f03` | PROJECT_STRUCTURE.md | docs file PROJECT_STRUCTURE.md (1340 bytes) |
| `ev_3e686e326561f485a5b7` | knowledge-base/decisions/SPEC.md | docs file knowledge-base/decisions/SPEC.md (192 bytes) |
| `ev_3e6cc82f52d45fec4feb` | TECH_STACK.md | docs file TECH_STACK.md (1192 bytes) |
| `ev_3eca9885c39c5fdbd1c7` | samples/requests/SPEC.md | docs file samples/requests/SPEC.md (355 bytes) |
| `ev_41a59dc8c183db91ce9d` | src/bosgenesis_mop_creation_agent/reconstruction/helm_hints.py | source file src/bosgenesis_mop_creation_agent/reconstruction/helm_hints.py (3064 bytes) |
| `ev_42586a8848ca25826927` | tests/test_artifact_writer_inventory.py | test file tests/test_artifact_writer_inventory.py (29274 bytes) |
| `ev_45dac091ca9d49acc345` | knowledge-base/design/SPEC.md | docs file knowledge-base/design/SPEC.md (104 bytes) |
| `ev_467480369ae920a5a21b` | src/bosgenesis_mop_creation_agent/mcp_clients/enrichment.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/enrichment.py (9463 bytes) |
| `ev_48dc84807fa2183be481` | docs/SAMPLE_REQUESTS.md | docs file docs/SAMPLE_REQUESTS.md (5143 bytes) |
| `ev_49b1dfb0184ff05ff4c0` | src/bosgenesis_mop_creation_agent/__init__.py | source file src/bosgenesis_mop_creation_agent/__init__.py (62 bytes) |
| `ev_4a8f3deb39656750680a` | artifacts/human-mop/SPEC.md | docs file artifacts/human-mop/SPEC.md (2238 bytes) |
| `ev_4f502f0e3deca1489453` | tests/contracts/SPEC.md | test file tests/contracts/SPEC.md (273 bytes) |
| `ev_52c25934b00154698419` | memory/SPEC.md | docs file memory/SPEC.md (631 bytes) |
| `ev_56995f7c8b6eda3f755d` | config/SPEC.md | docs file config/SPEC.md (572 bytes) |
| `ev_57fe4c3e33a5ad462600` | codex/config/config.toml | config file codex/config/config.toml (937 bytes) |
| `ev_597b80e4ee1706d7bcdd` | src/bosgenesis_mop_creation_agent/config/SPEC.md | docs file src/bosgenesis_mop_creation_agent/config/SPEC.md (4578 bytes) |
| `ev_5c5fabcc203e8d789db1` | src/bosgenesis_mop_creation_agent/collectors/SPEC.md | docs file src/bosgenesis_mop_creation_agent/collectors/SPEC.md (1181 bytes) |
| `ev_5d883be0cfb7f475cd79` | src/bosgenesis_mop_creation_agent/llm/__init__.py | source file src/bosgenesis_mop_creation_agent/llm/__init__.py (243 bytes) |
| `ev_5e1f3a8268ad05dd2927` | src/bosgenesis_mop_creation_agent/retrieval/reference_lookup.py | source file src/bosgenesis_mop_creation_agent/retrieval/reference_lookup.py (12202 bytes) |
| `ev_5e8158c70f38ab9a5e44` | tests/test_health.py | test file tests/test_health.py (1746 bytes) |
| `ev_5f27cef51d8e75038cb2` | tests/test_phase5_classification.py | test file tests/test_phase5_classification.py (6655 bytes) |
| `ev_61b1e1c93b24fdfa8bf1` | src/bosgenesis_mop_creation_agent/entrypoints/SPEC.md | docs file src/bosgenesis_mop_creation_agent/entrypoints/SPEC.md (960 bytes) |
| `ev_62aa4a2cbd94ae31c3ee` | src/bosgenesis_mop_creation_agent/models/requests.py | source file src/bosgenesis_mop_creation_agent/models/requests.py (2539 bytes) |
| `ev_64255b5847e3866a21b5` | codex/SPEC.md | docs file codex/SPEC.md (474 bytes) |
| `ev_64a15c7d3cb09e6bf262` | evaluations/SPEC.md | docs file evaluations/SPEC.md (303 bytes) |
| `ev_656cfb27f0fccb9063a5` | knowledge-base/interfaces/SPEC.md | docs file knowledge-base/interfaces/SPEC.md (252 bytes) |
| `ev_699e6760b342db3c25b0` | tests/test_phase9_qdrant_references.py | test file tests/test_phase9_qdrant_references.py (9989 bytes) |
| `ev_69f6dcc37ea40faffbaa` | memory/mongodb/SPEC.md | docs file memory/mongodb/SPEC.md (277 bytes) |
| `ev_6be9709a63fedad9ed8e` | knowledge-base/schemas/SPEC.md | docs file knowledge-base/schemas/SPEC.md (196 bytes) |
| `ev_6c9df83cad0b8316cd3c` | artifacts/human-mop/professional_mop_pdf_template.yaml | config file artifacts/human-mop/professional_mop_pdf_template.yaml (1794 bytes) |
| `ev_7319afc97f1faed777d2` | artifacts/installation-notes/SPEC.md | docs file artifacts/installation-notes/SPEC.md (1174 bytes) |
| `ev_7542ccdd9ec5f2619cc6` | certs/README.md | docs file certs/README.md (740 bytes) |
| `ev_7700f51e8255022bcb20` | tests/test_phase15_release_candidate.py | test file tests/test_phase15_release_candidate.py (2251 bytes) |
| `ev_775717382acafb855b86` | src/bosgenesis_mop_creation_agent/sources/snapshot_selector.py | source file src/bosgenesis_mop_creation_agent/sources/snapshot_selector.py (3372 bytes) |
| `ev_77d140b28ed3b8084f0b` | src/bosgenesis_mop_creation_agent/reconstruction/manifest_normalizer.py | source file src/bosgenesis_mop_creation_agent/reconstruction/manifest_normalizer.py (8191 bytes) |
| `ev_782f3cfd268c1cbf8b7f` | charts/bosgenesis-mop-creation-agent/templates/deployment.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/deployment.yaml (2581 bytes) |
| `ev_788604e61aa28f59f633` | tests/test_phase1_contract.py | test file tests/test_phase1_contract.py (15627 bytes) |
| `ev_7a1bffa2c3b95e857023` | charts/bosgenesis-mop-creation-agent/.helmignore | deployment file charts/bosgenesis-mop-creation-agent/.helmignore (65 bytes) |
| `ev_7b0f9943b88e386b954f` | knowledge-base/SPEC.md | docs file knowledge-base/SPEC.md (262 bytes) |
| `ev_7c9f8db437e40f22e15f` | src/bosgenesis_mop_creation_agent/models/responses.py | source file src/bosgenesis_mop_creation_agent/models/responses.py (2024 bytes) |
| `ev_7cc53e0e15675f7454d5` | .agents/skills/SKILLS.md | docs file .agents/skills/SKILLS.md (9902 bytes) |
| `ev_804c19db6dbeece95994` | src/bosgenesis_mop_creation_agent/reasoning/SPEC.md | docs file src/bosgenesis_mop_creation_agent/reasoning/SPEC.md (2231 bytes) |
| `ev_80dbdc7ffddd8021f593` | src/bosgenesis_mop_creation_agent/observability/models.py | source file src/bosgenesis_mop_creation_agent/observability/models.py (1517 bytes) |
| `ev_81491826abc400ce8f62` | docs/RELEASE_CANDIDATE_RUNBOOK.md | docs file docs/RELEASE_CANDIDATE_RUNBOOK.md (7686 bytes) |
| `ev_8181fabe1bdeb64638b9` | src/bosgenesis_mop_creation_agent/api/SPEC.md | docs file src/bosgenesis_mop_creation_agent/api/SPEC.md (5261 bytes) |
| `ev_83070dae6b2b9acaa230` | charts/bosgenesis-mop-creation-agent/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/SPEC.md (363 bytes) |
| `ev_85a0c65e4054357b293a` | pyproject.toml | config file pyproject.toml (1409 bytes) |
| `ev_866de4d6e31c0e368a47` | charts/bosgenesis-mop-creation-agent/templates/secret.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/secret.yaml (560 bytes) |
| `ev_879ba23766ad677f1210` | src/bosgenesis_mop_creation_agent/classification/__init__.py | source file src/bosgenesis_mop_creation_agent/classification/__init__.py (357 bytes) |
| `ev_885bcde5c491e80f2335` | src/bosgenesis_mop_creation_agent/models/SPEC.md | docs file src/bosgenesis_mop_creation_agent/models/SPEC.md (2302 bytes) |
| `ev_885d1765cb6312b6b720` | src/bosgenesis_mop_creation_agent/models/__init__.py | source file src/bosgenesis_mop_creation_agent/models/__init__.py (37 bytes) |
| `ev_89c6e98759d615624537` | src/bosgenesis_mop_creation_agent/reconstruction/models.py | source file src/bosgenesis_mop_creation_agent/reconstruction/models.py (1494 bytes) |
| `ev_8a68a6a600c7fd354070` | charts/bosgenesis-mop-creation-agent/Chart.yaml | deployment file charts/bosgenesis-mop-creation-agent/Chart.yaml (149 bytes) |
| `ev_8f9cfa26ca24a8cc4a11` | src/bosgenesis_mop_creation_agent/reconstruction/helm_values.py | source file src/bosgenesis_mop_creation_agent/reconstruction/helm_values.py (2361 bytes) |
| `ev_903cf04ac43aca5e9890` | src/bosgenesis_mop_creation_agent/api/routes.py | source file src/bosgenesis_mop_creation_agent/api/routes.py (13892 bytes) |
| `ev_916e745d563dda1c902b` | .github/workflows/SPEC.md | ci file .github/workflows/SPEC.md (574 bytes) |
| `ev_917b7e8f92d1d261d637` | reports/SPEC.md | docs file reports/SPEC.md (901 bytes) |
| `ev_94b8954436ec76d98112` | src/bosgenesis_mop_creation_agent/llm/model_gateway.py | source file src/bosgenesis_mop_creation_agent/llm/model_gateway.py (3217 bytes) |
| `ev_96cd759cc3bf8cb19af3` | src/bosgenesis_mop_creation_agent/__main__.py | source file src/bosgenesis_mop_creation_agent/__main__.py (105 bytes) |
| `ev_9a65b907f14c03274f36` | src/bosgenesis_mop_creation_agent/validation/SPEC.md | docs file src/bosgenesis_mop_creation_agent/validation/SPEC.md (1964 bytes) |
| `ev_9a8be3e20754fa86caf5` | certs/SPEC.md | docs file certs/SPEC.md (1369 bytes) |
| `ev_9b1b2e6de0923f28f5e0` | src/SPEC.md | docs file src/SPEC.md (2511 bytes) |
| `ev_9c6920ff0029a9ae310a` | tests/test_phase6_reconstruction.py | test file tests/test_phase6_reconstruction.py (14039 bytes) |
| `ev_9c7fb55fdd7971a64a6b` | memory/redis/SPEC.md | docs file memory/redis/SPEC.md (390 bytes) |
| `ev_9ee3faa4a9a9dd7eed44` | SPEC.md | docs file SPEC.md (1808 bytes) |
| `ev_a4a53dd3c9639fe4dd55` | LICENSE | other file LICENSE (2417 bytes) |
| `ev_a4d3988232175c4045ba` | charts/bosgenesis-mop-creation-agent/templates/pvc.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/pvc.yaml (680 bytes) |
| `ev_a5b7f249e1d06a78872f` | docs/SPEC.md | docs file docs/SPEC.md (3905 bytes) |
| `ev_a6696c840a52957323a6` | src/bosgenesis_mop_creation_agent/observability/__init__.py | source file src/bosgenesis_mop_creation_agent/observability/__init__.py (213 bytes) |
| `ev_a6c3b965a387d3030e40` | deploy/k8s/SPEC.md | deployment file deploy/k8s/SPEC.md (219 bytes) |
| `ev_aaf91001d9083b18a9d7` | playbook/deploy.sh | source file playbook/deploy.sh (8003 bytes) |
| `ev_ab6a7ba99af51b8af39f` | src/bosgenesis_mop_creation_agent/memory/service.py | source file src/bosgenesis_mop_creation_agent/memory/service.py (8584 bytes) |
| `ev_abe1919ac01e8f2db926` | src/bosgenesis_mop_creation_agent/core/orchestrator.py | source file src/bosgenesis_mop_creation_agent/core/orchestrator.py (36273 bytes) |
| `ev_adcf006b16182e99d821` | src/bosgenesis_mop_creation_agent/retrieval/SPEC.md | docs file src/bosgenesis_mop_creation_agent/retrieval/SPEC.md (1991 bytes) |
| `ev_adcf4cca0c9b94a00fb7` | src/bosgenesis_mop_creation_agent/retrieval/models.py | source file src/bosgenesis_mop_creation_agent/retrieval/models.py (1771 bytes) |
| `ev_ae053c52532bc8d2071c` | src/bosgenesis_mop_creation_agent/memory/__init__.py | source file src/bosgenesis_mop_creation_agent/memory/__init__.py (267 bytes) |
| `ev_ae346ce820a17cbe4193` | docs/CONTEXT_SNAPSHOT.md | docs file docs/CONTEXT_SNAPSHOT.md (7259 bytes) |
| `ev_ae8cf4640a2f59133733` | docs/01_SPEC_MOP_CREATION_AGENT.md | docs file docs/01_SPEC_MOP_CREATION_AGENT.md (25454 bytes) |
| `ev_af038e2a54c567bf3aa4` | src/bosgenesis_mop_creation_agent/llm/repair_suggester.py | source file src/bosgenesis_mop_creation_agent/llm/repair_suggester.py (11083 bytes) |
| `ev_af2be7168cb0efc9f8d0` | charts/bosgenesis-mop-creation-agent/values.credentials.example.yaml | deployment file charts/bosgenesis-mop-creation-agent/values.credentials.example.yaml (596 bytes) |
| `ev_b3d4caa93e9f68c65175` | .agents/skills/SKILL.md | docs file .agents/skills/SKILL.md (8207 bytes) |
| `ev_b42f676a61a37666f3d4` | src/bosgenesis_mop_creation_agent/sources/snapshot_models.py | source file src/bosgenesis_mop_creation_agent/sources/snapshot_models.py (1811 bytes) |
| `ev_b4a45e091322e847793f` | playbook/validation/SPEC.md | docs file playbook/validation/SPEC.md (300 bytes) |
| `ev_b4d707d49956529a42ad` | charts/bosgenesis-mop-creation-agent/templates/ingress.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/ingress.yaml (991 bytes) |
| `ev_b718f7060805bb532f3b` | src/bosgenesis_mop_creation_agent/config/settings.py | source file src/bosgenesis_mop_creation_agent/config/settings.py (15051 bytes) |
| `ev_b71e1a2c8c082140b74b` | tests/e2e/SPEC.md | test file tests/e2e/SPEC.md (294 bytes) |
| `ev_b8bb204b6832d537d288` | deploy/k8s/overlays/SPEC.md | deployment file deploy/k8s/overlays/SPEC.md (185 bytes) |
| `ev_b9e130c311ca345a252e` | src/bosgenesis_mop_creation_agent/core/SPEC.md | docs file src/bosgenesis_mop_creation_agent/core/SPEC.md (4204 bytes) |
| `ev_bb8f25c646298133da0c` | src/bosgenesis_mop_creation_agent/api/mcp.py | source file src/bosgenesis_mop_creation_agent/api/mcp.py (7200 bytes) |
| `ev_bcedb79e4c27c1f614b5` | memory/clickhouse/SPEC.md | docs file memory/clickhouse/SPEC.md (318 bytes) |
| `ev_beff559c0b1b4d9fb21f` | tests/test_snapshot_selector.py | test file tests/test_snapshot_selector.py (3163 bytes) |
| `ev_bffdd593e9e29736782e` | src/bosgenesis_mop_creation_agent/reconstruction/planner.py | source file src/bosgenesis_mop_creation_agent/reconstruction/planner.py (11834 bytes) |
| `ev_c086cf52fd8046c885cc` | src/bosgenesis_mop_creation_agent/rendering/pdf_renderer.py | source file src/bosgenesis_mop_creation_agent/rendering/pdf_renderer.py (39550 bytes) |
| `ev_c28896ae9d8ef82e3f80` | docs/07_SAMPLE_MOP_TEMPLATE.md | docs file docs/07_SAMPLE_MOP_TEMPLATE.md (3754 bytes) |
| `ev_c38db9281c4696e54e44` | src/bosgenesis_mop_creation_agent/classification/resource_classifier.py | source file src/bosgenesis_mop_creation_agent/classification/resource_classifier.py (9076 bytes) |
| `ev_c6aa11ff5f210bf187f3` | docs/04_ALGORITHM_MOP_CREATION_AGENT.md | docs file docs/04_ALGORITHM_MOP_CREATION_AGENT.md (28900 bytes) |
| `ev_c7fb20472714d6ec182e` | evaluations/grounding/SPEC.md | docs file evaluations/grounding/SPEC.md (161 bytes) |
| `ev_c8e3ca4a23de78035063` | tests/test_phase11_memory_layer.py | test file tests/test_phase11_memory_layer.py (7555 bytes) |
| `ev_c97a1cba1d41cf9cc3a5` | src/bosgenesis_mop_creation_agent/reconstruction/__init__.py | source file src/bosgenesis_mop_creation_agent/reconstruction/__init__.py (132 bytes) |
| `ev_ca3ee59990c693f129b6` | playbook/SPEC.md | docs file playbook/SPEC.md (220 bytes) |
| `ev_cb5b41071ab66dcee7e4` | src/bosgenesis_mop_creation_agent/memory/SPEC.md | docs file src/bosgenesis_mop_creation_agent/memory/SPEC.md (3714 bytes) |
| `ev_cb6960661c7dd343e35e` | charts/bosgenesis-mop-creation-agent/templates/configmap.yaml | deployment file charts/bosgenesis-mop-creation-agent/templates/configmap.yaml (779 bytes) |
| `ev_cc4e3293606a3f3486ec` | charts/bosgenesis-mop-creation-agent/values/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/values/SPEC.md (310 bytes) |
| `ev_ce201c651209346563ce` | src/bosgenesis_mop_creation_agent/mcp_clients/SPEC.md | docs file src/bosgenesis_mop_creation_agent/mcp_clients/SPEC.md (1594 bytes) |
| `ev_ce2fe2ffc313a83d8fe1` | docs/K8S_INSPECTOR_RESOURCE_DETAIL_ENRICHMENT_PLAN.md | docs file docs/K8S_INSPECTOR_RESOURCE_DETAIL_ENRICHMENT_PLAN.md (8029 bytes) |
| `ev_d0460b2cc9a5077efec2` | src/bosgenesis_mop_creation_agent/mcp_clients/k8s_inspector_client.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/k8s_inspector_client.py (7628 bytes) |
| `ev_d2152fe30d775da505f9` | .gitignore | config file .gitignore (218 bytes) |
| `ev_d22e6ffada3f12f7ad05` | certs/.gitkeep | other file certs/.gitkeep (1 bytes) |
| `ev_d2a06bcbfc4d69f38b67` | src/bosgenesis_mop_creation_agent/persistence/SPEC.md | docs file src/bosgenesis_mop_creation_agent/persistence/SPEC.md (1919 bytes) |
| `ev_d402ee6854e999a72c84` | src/bosgenesis_mop_creation_agent/entrypoints/__init__.py | source file src/bosgenesis_mop_creation_agent/entrypoints/__init__.py (28 bytes) |
| `ev_d403ffc127f56c7db719` | .agents/skills/SPEC.md | docs file .agents/skills/SPEC.md (265 bytes) |
| `ev_d480c47b73d0c18286db` | src/bosgenesis_mop_creation_agent/mcp_clients/base.py | source file src/bosgenesis_mop_creation_agent/mcp_clients/base.py (8295 bytes) |
| `ev_d5f81b9e14843b2a96be` | codex/prompts/SPEC.md | docs file codex/prompts/SPEC.md (313 bytes) |
| `ev_d7fb107d38c08abfc3b5` | docs/03_LLD_MOP_CREATION_AGENT.md | docs file docs/03_LLD_MOP_CREATION_AGENT.md (23592 bytes) |
| `ev_d8ca2e0f7f24a2f6de97` | codex/config/SPEC.md | docs file codex/config/SPEC.md (186 bytes) |
| `ev_d904ca554295c74a0178` | samples/SPEC.md | docs file samples/SPEC.md (431 bytes) |
| `ev_da9fb4ad17600c5fe98e` | docs/kubernetes-mop-sample.md | docs file docs/kubernetes-mop-sample.md (9285 bytes) |
| `ev_db190aa4b3118ab3a28a` | charts/bosgenesis-mop-creation-agent/templates/SPEC.md | deployment file charts/bosgenesis-mop-creation-agent/templates/SPEC.md (218 bytes) |
| `ev_dd42cec2cc80744b3307` | docs/02_HLD_MOP_CREATION_AGENT.md | docs file docs/02_HLD_MOP_CREATION_AGENT.md (14244 bytes) |
| `ev_dda6685f008fc2f86b51` | knowledge-base/session/SPEC.md | docs file knowledge-base/session/SPEC.md (199 bytes) |
| `ev_dfe457c907b8ff865b98` | docs/06_APPLICATION_MODE.md | docs file docs/06_APPLICATION_MODE.md (7498 bytes) |
| `ev_e12e86b0a352933eeec6` | tests/test_phase4_mcp_enrichment.py | test file tests/test_phase4_mcp_enrichment.py (10444 bytes) |
| `ev_e3655316bd877fa6be15` | src/bosgenesis_mop_creation_agent/common/logging.py | source file src/bosgenesis_mop_creation_agent/common/logging.py (1803 bytes) |
| `ev_e3783521b07d99172c1f` | tests/test_phase10_bounded_reasoning.py | test file tests/test_phase10_bounded_reasoning.py (9367 bytes) |
| `ev_e4932fc2064e8da4f4dc` | .github/workflows/ci.yml | ci file .github/workflows/ci.yml (1079 bytes) |
| `ev_e5c5040ed911b457a188` | samples/requests/platform-only-generate.json | config file samples/requests/platform-only-generate.json (379 bytes) |
| `ev_ea04bad51e72f69966f5` | codex/skills/SPEC.md | docs file codex/skills/SPEC.md (221 bytes) |
| `ev_eca55fb783a9582a2580` | src/bosgenesis_mop_creation_agent/config/__init__.py | source file src/bosgenesis_mop_creation_agent/config/__init__.py (38 bytes) |
| `ev_edf83e1e68fd2ab54c20` | playbook/deployment/SPEC.md | docs file playbook/deployment/SPEC.md (303 bytes) |
| `ev_ef42a55d5022b1eddba1` | .github/SPEC.md | docs file .github/SPEC.md (272 bytes) |
| `ev_f1427029e213e79d544b` | artifacts/SPEC.md | docs file artifacts/SPEC.md (449 bytes) |
| `ev_f14da9fc9652c183f3ad` | memory/postgresql/SPEC.md | docs file memory/postgresql/SPEC.md (477 bytes) |
| `ev_f31189a1753147077f49` | src/bosgenesis_mop_creation_agent/observability/SPEC.md | docs file src/bosgenesis_mop_creation_agent/observability/SPEC.md (2536 bytes) |
| `ev_f3dceef3dfb8c9cdcef8` | src/bosgenesis_mop_creation_agent/reconstruction/quality_gate.py | source file src/bosgenesis_mop_creation_agent/reconstruction/quality_gate.py (2454 bytes) |
| `ev_f3eea28938c6d6e24853` | .dockerignore | config file .dockerignore (103 bytes) |
| `ev_f4ef8c15ee53e883ffd6` | src/bosgenesis_mop_creation_agent/common/SPEC.md | docs file src/bosgenesis_mop_creation_agent/common/SPEC.md (714 bytes) |
| `ev_f79cadad51e2b8de71ef` | src/bosgenesis_mop_creation_agent/retrieval/component_query_builder.py | source file src/bosgenesis_mop_creation_agent/retrieval/component_query_builder.py (5788 bytes) |
| `ev_faea43427c013b484a72` | playbook/uninstaller.sh | source file playbook/uninstaller.sh (3091 bytes) |
| `ev_fc1de4df23348bbb6d27` | codex/skills/SKILL.md | docs file codex/skills/SKILL.md (2712 bytes) |
| `ev_fe80c2322398ac7cb083` | memory/langmem/SPEC.md | docs file memory/langmem/SPEC.md (275 bytes) |

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
- Overall risk: `medium`
- Summary: Static scan identified 2 common vulnerability signal(s) for human review.
- Safe reasoning summary: Reviewed static vulnerability findings, dependency manifests, and quality scan status for common risk themes.
