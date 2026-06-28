# Method of Procedure: bosgenesis

## 1. Document Control
- Workflow: MoP Generation
- Namespace: `bosgenesis`
- Environment: `kubernetes_generic`
- Helm Release: `Not selected`
- Status: Draft for human review

## 2. Change Summary
Generate MoP in both markdown and PDF format so we can fully clone the source namespace

## 3. Target Namespace and Environment
- Namespace: `bosgenesis`
- Environment: `kubernetes_generic`

## 4. Scope and Assumptions
- This workflow produces a human-reviewed clone MoP package in Markdown and PDF format.
- Evidence collection and document generation are read-only; Kubernetes or Helm mutations are not performed here.
- Human approval is required before any execution workflow uses this document.

## 5. Source Evidence
- k8s-inspector: `limited` - Server error '503 Service Temporarily Unavailable' for url 'http://k8s-inspector.bosgenesis.local/mcp/tools/namespace_summary'
For more information check: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/503
- helm-manager: `limited` - Client error '404 Not Found' for url 'http://helm-manager.bosgenesis.local/mcp/tools/list_releases'
For more information check: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404
- mop-creation-agent: `limited` - MCP tool not found: mop_create_draft

## 6. Current State Summary
Evidence was collected from configured MCP adapters when available. Missing adapters are listed
under limitations.

## 7. Preconditions and Readiness Checks
- Confirm namespace `bosgenesis` is the intended target.
- Confirm Helm release `Not selected` or select the correct release before execution.
- Confirm operator has access to required dashboards and rollback evidence.

## 8. Risk Assessment Matrix
| Risk | Impact | Mitigation |
|---|---|---|
| Missing live evidence | Medium | Review MCP limitations before execution. |
| Namespace mismatch | High | Validate namespace allowlist and owner approval. |
| Rollback ambiguity | High | Confirm Helm revision and rollback command. |

## 9. Implementation Steps
1. Review current namespace and Helm evidence.
2. Confirm implementation window and stakeholders.
3. Execute only through a future approved MoP Execution workflow.

## 10. Validation Steps
1. Validate workloads and services after execution.
2. Confirm ingress and service endpoints respond as expected.
3. Capture post-change evidence for audit.

## 11. Rollback Plan
1. Stop execution if validation fails.
2. Use approved Helm/Kubernetes rollback procedure after human approval.
3. Re-run validation checks and capture evidence.

## 12. Communication Plan
- Notify platform owner before execution.
- Notify stakeholders after validation or rollback.

## 13. Approval and Human Review Notes
- This draft is not an execution approval.
- Human reviewer must confirm risk, rollback, and implementation steps.

## 14. Execution Readiness Decision
Needs review before execution.

## 15. Agent Activity and Safe Reasoning Summaries
- MoP was generated from selected namespace, user intent, and available MCP evidence.
- Limitations:
- k8s-inspector evidence limited: Server error '503 Service Temporarily Unavailable' for url 'http://k8s-inspector.bosgenesis.local/mcp/tools/namespace_summary'
For more information check: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/503
- helm-manager evidence limited: Client error '404 Not Found' for url 'http://helm-manager.bosgenesis.local/mcp/tools/list_releases'
For more information check: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404
- mop-creation-agent evidence limited: MCP tool not found: mop_create_draft
