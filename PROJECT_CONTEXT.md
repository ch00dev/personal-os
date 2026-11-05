# Personal OS — Project Context

## 1. Product Vision

Personal OS is a personal productivity and life-management platform designed to function as a second brain and an intelligent personal operating system.

Its purpose is to centralize information, organize responsibilities, manage projects and goals, track progress, and help the user make better decisions.

The platform should reduce cognitive overload, improve prioritization and turn ideas into consistent execution.

It is not just a task manager. It should connect the different areas of life into one coherent system.

## 2. Main Problems

- Too many ideas and simultaneous responsibilities.
    
- Difficulty prioritizing what matters.
    
- Information scattered across different applications.
    
- Lack of a unified view of goals, projects and tasks.
    
- Difficulty maintaining consistent execution.
    
- Limited visibility into personal progress and finances.
    

## 3. Main Product Areas

### Dashboard

A central overview of priorities, tasks, projects, goals, calendar events and relevant metrics.

### Areas of Life

Organize responsibilities into areas such as education, career, work, finances, health, personal development and projects.

### Tasks

Capture, organize, prioritize and track tasks. Support deadlines, status, projects, areas and recurring tasks.

### Projects

Manage projects, milestones, tasks, progress and related information.

### Goals

Define objectives, measurable outcomes, deadlines and progress indicators.

### Knowledge Base

Store notes, ideas, references, documents and useful information. Support search and relationships between knowledge and projects.

### Personal Finance

Record income, expenses and financial goals. Start with manual text or audio capture and user confirmation before saving.

### AI Assistant

An intelligent assistant that understands natural language, organizes information, answers questions, analyzes priorities and helps with planning.

### Integrations

Potential integrations include Telegram, Google Calendar, Gmail and other services.

## 4. AI Experience

The assistant should eventually support:

- Text and audio capture.
    
- Automatic classification of ideas, tasks and notes.
    
- Contextual search across personal information.
    
- Daily and weekly planning.
    
- Project progress analysis.
    
- Suggestions for priorities and next actions.
    
- Reports and proactive insights.
    

AI must not independently make consequential changes.

The system should distinguish between:

1. Understanding and suggesting.
    
2. Preparing an action.
    
3. Validating the action.
    
4. Asking for confirmation when necessary.
    
5. Executing through trusted backend logic.
    

## 5. Initial Technical Direction

Frontend:

- Next.js App Router
    
- React
    
- TypeScript
    
- Material UI
    
- TanStack Query
    
- React Hook Form
    
- Zod
    

Backend:

- Python
    
- FastAPI
    
- Pydantic
    
- SQLAlchemy
    
- Alembic
    

Data:

- PostgreSQL
    
- pgvector when semantic search becomes necessary
    

AI:

- Pydantic AI as an initial agent framework
    
- Ollama for local model experimentation
    
- Optional external model providers through an abstraction layer
    

Infrastructure:

- Docker
    
- WSL2 on Windows
    
- Git and GitHub
    

Integrations:

- Telegram Bot API
    
- n8n when workflow automation becomes useful
    

These are initial technology choices, not permanent requirements. Verify current stable versions and compatibility before implementation.

## 6. Architectural Principles

- Start with a modular monolith.
    
- Keep PostgreSQL as the source of truth.
    
- Use clear boundaries between modules.
    
- Build an API-first backend.
    
- Prioritize data ownership and privacy.
    
- Prefer local development initially.
    
- Keep the system extensible without premature complexity.
    
- Use migrations and automated tests.
    
- Avoid unnecessary infrastructure.
    

## 7. Development Strategy

Build the product incrementally.

Start with a functional core:

1. Authentication and user configuration.
    
2. Areas of life.
    
3. Tasks and projects.
    
4. Goals.
    
5. Dashboard.
    
6. Initial AI assistant.
    

Then evolve into:

- Knowledge management.
    
- Telegram capture.
    
- Audio processing.
    
- Calendar and email integrations.
    
- Financial management.
    
- Advanced AI planning and analytics.
    

Do not implement every idea in the first version.

## 8. Product Philosophy

The system should be:

- Useful in everyday life.
    
- Fast and intuitive.
    
- Reliable and secure.
    
- Easy to maintain.
    
- Modular and extensible.
    
- Affordable to operate.
    
- Designed around real workflows, not unnecessary features.
    

The priority is to build something that genuinely improves daily execution, not simply an impressive technical demonstration.

## 9. Important Development Rule

Every new feature should answer:

- What problem does it solve?
    
- Who or what benefits from it?
    
- How does it connect to existing modules?
    
- What data does it need?
    
- What is the simplest reliable implementation?
    
- Is it necessary for the current stage?