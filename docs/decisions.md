# Personal OS — Architecture Decision Records

This document tracks important architectural and technical decisions.

## ADR-001 — Modular Monolith

Status: Accepted

Decision:  
Start with a modular monolith instead of microservices.

Reason:  
The project is initially developed by one person. A modular monolith reduces operational complexity while preserving internal separation.

## ADR-002 — PostgreSQL as the Source of Truth

Status: Accepted

Decision:  
Use PostgreSQL as the primary database.

Reason:  
It supports relational data, transactions, constraints and future extensibility.

## ADR-003 — FastAPI Backend

Status: Accepted

Decision:  
Use Python and FastAPI for the backend.

Reason:  
Strong Python ecosystem, API development experience, data processing and AI integration.

## ADR-004 — Next.js Frontend

Status: Accepted

Decision:  
Use Next.js, React and TypeScript.

Reason:  
Modern frontend ecosystem, reusable components, strong tooling and maintainability.

## ADR-005 — AI Does Not Bypass Business Logic

Status: Accepted

Decision:  
AI can interpret, recommend and prepare actions, but backend services validate and execute them.

Reason:  
Reliability, security, predictable behavior and user control.

## ADR-006 — Local-First Development

Status: Accepted

Decision:  
Start with local development using Docker and WSL2.

Reason:  
Lower operating costs, easier experimentation and control over development data.

## ADR-007 — Avoid Premature Infrastructure

Status: Accepted

Decision:  
Do not introduce Redis, Kafka, Kubernetes or microservices until a measurable requirement justifies them.

Reason:  
Reduce complexity and focus development effort on product value.

## Future Decisions

Record new decisions using this structure:

### ADR-XXX — Decision Title

Status: Proposed / Accepted / Rejected / Superseded

Context:  
What problem or requirement led to this decision?

Decision:  
What was chosen?

Alternatives:  
What other options were considered?

Consequences:  
What are the benefits, trade-offs and limitations?

Date:  
YYYY-MM-DD