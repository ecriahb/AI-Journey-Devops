# Final Project — AI DevOps Troubleshooting / RCA Agent

## Objective
Build an enterprise-style agent that investigates CI/CD and AKS deployment failures using trusted evidence.

## Inputs
- GitHub / Azure DevOps pipeline logs
- Terraform plan/apply output
- AKS events and pod logs
- Azure Monitor metrics
- Last successful deployment/context

## Flow
```text
Failure
  ↓
Collect Evidence
  ↓
Classify / Prioritize
  ↓
Investigate with approved tools
  ↓
Grounded RCA
  ↓
Recommended Fix
  ↓
Human Approval
  ↓
Approved Remediation
```

## Guardrails
- No secret leakage
- Read-only investigation by default
- No destructive automatic actions
- Evidence preserved outside the model conversation
- Structured RCA output
- Human approval before risky changes
- Audit logs and least privilege

## Final outcome
A portfolio-ready Agentic DevOps system demonstrating Python, LLMs, RAG, tool calling, MCP, LangGraph, multi-agent patterns and MLOps/production practices.
