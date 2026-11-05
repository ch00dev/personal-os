# AGENTS.md — Development Instructions

## 1. Project Context

Before making changes, read:

- `PROJECT_CONTEXT.md`
    
- `README.md`
    
- Relevant documents inside `docs/`
    

These files define the product vision, requirements, architecture, roadmap and technical decisions.

## 2. General Principles

- Build a reliable, maintainable and secure product.
    
- Prefer simplicity over unnecessary complexity.
    
- Use modern, stable and well-supported technologies.
    
- Follow official documentation and current best practices.
    
- Avoid premature optimization and overengineering.
    
- Prefer open-source and low-cost solutions when appropriate.
    
- Do not introduce unnecessary dependencies or infrastructure.
    

## 3. Architecture

- Start with a modular monolith.
    
- Keep frontend, backend and business logic clearly separated.
    
- PostgreSQL is the source of truth.
    
- AI interprets, organizes and recommends; backend logic validates and executes.
    
- Keep modules independent and maintain clear interfaces.
    
- Do not introduce microservices, Redis, Kafka or Kubernetes without a concrete need.
    

## 4. Development Workflow

Before implementing a significant feature:

1. Understand the requirement.
    
2. Inspect the existing code.
    
3. Identify affected modules.
    
4. Propose a concise implementation plan.
    
5. Implement in small, testable steps.
    
6. Run relevant tests and checks.
    
7. Update documentation when necessary.
    

Do not rewrite working code unnecessarily.

## 5. Code Quality

- Use clear naming and consistent conventions.
    
- Add type hints and validation.
    
- Keep functions and components focused.
    
- Handle errors explicitly.
    
- Avoid duplicated logic.
    
- Write tests for important business rules.
    
- Never leave secrets or credentials in source code.
    

## 6. Frontend

- Use TypeScript.
    
- Follow existing component and styling conventions.
    
- Prefer reusable components.
    
- Validate forms and handle loading, empty and error states.
    
- Keep the interface responsive and accessible.
    

## 7. Backend

- Use FastAPI and Pydantic.
    
- Follow clear separation between API routes, services and data access.
    
- Use SQLAlchemy and Alembic for database operations.
    
- Validate all incoming data.
    
- Enforce authorization on the backend.
    

## 8. Database

- Use PostgreSQL as the primary database.
    
- Make schema changes through Alembic migrations.
    
- Preserve data integrity and use appropriate constraints.
    
- Never make destructive database changes without explicit approval.
    

## 9. AI and Automation Safety

- Treat model outputs as untrusted input.
    
- Validate AI-generated actions before execution.
    
- Require user confirmation for consequential actions.
    
- Never expose private information, API keys or credentials.
    
- Keep an audit trail for important operations.
    

## 10. Communication

- Explain important technical decisions clearly.
    
- Tell me when an idea is unnecessarily complex.
    
- Identify trade-offs and risks.
    
- Do not pretend something works without testing it.
    
- If requirements are ambiguous, ask before making major assumptions.
    

## 11. Documentation

Keep `PROJECT_CONTEXT.md`, `README.md` and relevant documents in `docs/` updated as the project evolves.

Do not silently contradict established architectural decisions. If a decision should change, explain why and propose an update to `docs/decisions.md`.