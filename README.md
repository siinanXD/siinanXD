# Hi, I'm Sinan

**AI Engineer with 7 years in industrial automation** — I build production-oriented AI systems with agent workflows, RAG, human-in-the-loop controls, and reliable software engineering around them.

Germany · [LinkedIn](https://www.linkedin.com/in/kahraman-sinan/) · [sjcode.de](https://sjcode.de)

---

## Featured Projects

### [Mail Agent](https://github.com/siinanXD/Mail-agent)
[![CI](https://github.com/siinanXD/Mail-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/Mail-agent/actions/workflows/ci.yml)

Agent for vacation-rental mailboxes. Watches an IMAP inbox, recognises bookings, cancellations, changes and guest messages, assigns them to the right property without duplicates, and answers questions in natural language through nine SQL and vector tools. Counts always come from SQL, meaning from pgvector, never the other way round. Every extracted value is shown against the original mail as literal or inferred. Multi-tenant with PostgreSQL row-level security, weekly cleaning plans to staff via WhatsApp, 292 tests run in CI against a real PostgreSQL.

> Python · FastAPI · LangChain · OpenAI · PostgreSQL/pgvector · Alembic · Langfuse · Twilio · Docker

### [Maintenance AI Assistant](https://github.com/siinanXD/maintenance-ai-assistant)
[![CI](https://github.com/siinanXD/maintenance-ai-assistant/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/maintenance-ai-assistant/actions/workflows/ci.yml)

Full-stack AI system for industrial maintenance teams. A technician reports a fault with a photo at the machine, a work order is raised from it, spare parts are booked against the order, and legally required inspections (DGUV V3, BetrSichV) are documented with proof. Shift planning follows German working-time rules. A tool-using assistant answers from the plant's own data and manuals, always names its sources, and needs user confirmation before it writes anything. 661 tests with a 75 % coverage gate, 39 Alembic migrations, runs without an API key through a local mock provider.

> Python · Flask · SQLAlchemy · PostgreSQL/pgvector · OpenAI-compatible providers · React · TypeScript · Docker

### [Document Intelligence MVP](https://github.com/siinanXD/document-intelligence-mvp)

Multi-tenant document intelligence service. Documents are uploaded, parsed into a normalized representation, chunked with provenance, embedded, indexed for semantic search, and answered over with grounded citations. "The documents do not say" is a valid answer, and conflicting passages are returned as conflicting rather than smoothed over. 595 tests in 62 files, 12 Alembic migrations, and two CI workflows including a merge gate. The evaluation dataset ships with its own licence and provenance, and privacy tests assert that API keys never reach logs or traces.

> Python · FastAPI · PostgreSQL · Qdrant · Docling · Alembic · RAG · multi-tenancy · GitHub Actions

### [Agent Eval Harness](https://github.com/siinanXD/agent-eval-harness)
[![CI](https://github.com/siinanXD/agent-eval-harness/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/agent-eval-harness/actions/workflows/ci.yml)

Deterministic regression gates for LLM agent behaviour, across providers, in CI. Scores generation and retrieval separately, stores each run, and fails the build when results regress against the last known-good baseline. No LLM judge in the gate — every scorer returns the same score for the same output, so a moved number always means the agent moved.

> Python · evaluation · multi-provider · regression testing · CI · RAG · standard-library-only

### [Booking Email Platform](https://github.com/siinanXD/Booking-email-check)
AI-powered email processing for vacation-rental operations. Classifies incoming mail, extracts booking data, drafts replies, and keeps a mandatory human approval step before sending. Includes multi-tenancy, WhatsApp notifications, observability, CI, and Railway deployment.

> Python · Flask · LangGraph · MongoDB Atlas · React · TypeScript · Langfuse · Railway

### [Online Lerncampus](https://github.com/siinanXD/Online-Lerncampus)
Privacy-conscious learning platform for technical apprenticeships with a structured curriculum, exam-style questions, progress tracking, content-generation workflows, and review gates for AI-generated learning material.

> FastAPI · Python · Learning analytics · Privacy-by-design · Content workflows

### [sjcode.de](https://github.com/siinanXD/SJCODE-website)
My software and AI automation website, built as a performant Next.js application with SEO-focused structured data and a production deployment workflow.

> Next.js · React · TypeScript · Netlify

---

## Engineering Focus

**Agent Systems:** durable workflows, tool use, human approval, provider routing, auditability

**AI Engineering:** RAG, retrieval pipelines, structured outputs, evaluation, observability, guardrails

**Backend:** Python, FastAPI, Flask, SQLAlchemy, REST APIs, background jobs

**Data:** PostgreSQL, pgvector, MongoDB, Redis, SQLite

**Frontend:** React, TypeScript, Next.js, Tailwind CSS

**Production:** Docker, GitHub Actions, Railway, CI/CD, typing, testing, secret-safe configuration

---

## Current Direction

I am currently concentrating on reusable AI-engineering infrastructure rather than isolated demo applications:

- agent runtime patterns for resumable, approval-gated workflows
- secure MCP/tool integration patterns
- production RAG with measurable retrieval quality
- context engineering with `AGENTS.md`, architecture decisions, and structured project knowledge
- privacy-safe automation that separates private operational context from publishable reference implementations

---

## How I Build

- Human-in-the-loop for consequential AI actions
- Tests, linting, typing, and build checks as release gates
- Explicit architecture and decision records instead of hidden conventions
- No secrets or private operational data in public repositories
- Demo and local-fallback modes where practical so projects can be evaluated without production credentials
