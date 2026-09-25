# Hi, I'm Sinan

**AI Engineer with 7 years in industrial automation.** I spent six years as an electronics technician for industrial systems (Elektroniker für Betriebstechnik) before moving into AI engineering. I build AI systems for the shop floor: maintenance assistants, document intelligence for machine manuals and electrical drawings, and agents that act on real operational data with a human in the loop.

Euskirchen, Germany · [LinkedIn](https://www.linkedin.com/in/kahraman-sinan/) · [sjcode.de](https://sjcode.de)

---

## Featured Projects

### [Maintenance AI Assistant](https://github.com/siinanXD/maintenance-ai-assistant)
[![CI](https://github.com/siinanXD/maintenance-ai-assistant/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/maintenance-ai-assistant/actions/workflows/ci.yml)

Full-stack AI system for industrial maintenance teams. A technician reports a fault with a photo at the machine, a work order is raised from it, spare parts are booked against the order, and legally required inspections (DGUV V3, BetrSichV) are documented with proof. Shift planning follows German working-time rules. A tool-using assistant answers from the plant's own data and manuals, always names its sources, and needs user confirmation before it writes anything.

**Try it in 2 minutes:** runs without an API key through a local mock provider (`docker compose up`). 661 tests with a 75 % coverage gate, 39 Alembic migrations.

> Python · Flask · SQLAlchemy · PostgreSQL/pgvector · OpenAI-compatible providers · React · TypeScript · Docker

### [Document Intelligence MVP](https://github.com/siinanXD/document-intelligence-mvp)

Multi-tenant document intelligence service, built for technical documentation: manuals, datasheets, inspection reports. Documents are uploaded, parsed into a normalized representation, chunked with provenance, embedded, indexed for semantic search, and answered over with grounded citations. "The documents do not say" is a valid answer, and conflicting passages are returned as conflicting rather than smoothed over. 595 tests, 12 Alembic migrations, two CI workflows including a merge gate. Privacy tests assert that API keys never reach logs or traces.

> Python · FastAPI · PostgreSQL · Qdrant · Docling · Alembic · RAG · multi-tenancy · GitHub Actions

### [Mail Agent](https://github.com/siinanXD/Mail-agent)
[![CI](https://github.com/siinanXD/Mail-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/Mail-agent/actions/workflows/ci.yml)

Agent for vacation-rental mailboxes. Watches an IMAP inbox, recognises bookings, cancellations, changes and guest messages, assigns them to the right property without duplicates, and answers questions in natural language through nine SQL and vector tools. Counts always come from SQL, meaning from pgvector, never the other way round. Every extracted value is shown against the original mail as literal or inferred. Multi-tenant with PostgreSQL row-level security, 292 tests run in CI against a real PostgreSQL.

> Python · FastAPI · LangChain · OpenAI · PostgreSQL/pgvector · Alembic · Langfuse · Twilio · Docker

More repositories: [Agent Eval Harness](https://github.com/siinanXD/agent-eval-harness) (deterministic regression gates for agent behaviour in CI) · [Online Lerncampus](https://github.com/siinanXD/Online-Lerncampus) · [sjcode.de](https://github.com/siinanXD/SJCODE-website)

---

## Current Direction: AI for Industry 4.0

I am building AI applications for manufacturing and the German Mittelstand, where I know the domain from the inside:

- **Electrical documentation assistant** (in progress): a chatbot over circuit diagrams, terminal plans, parts lists and Siemens STEP 7 AWL programs that tracks devices (`-K12`), terminals (`-X1:5`) and PLC addresses (`E0.0`) across all documents
- **Maintenance and inspection workflows** with legal proof (DGUV V3, BetrSichV) and a human approval step before anything is written
- **Grounded RAG over machine manuals** with citations, measurable retrieval quality and "the documents do not say" as an honest answer
- **Predictive maintenance and anomaly detection** on machine and sensor data

---

## Engineering Focus

**Industrial domain:** electrical drawings, PLC (Siemens STEP 7), maintenance processes, inspection law, shift planning

**Agent Systems:** durable workflows, tool use, human approval, provider routing, auditability

**AI Engineering:** RAG, retrieval pipelines, structured outputs, evaluation, observability, guardrails

**Backend & Data:** Python, FastAPI, Flask, SQLAlchemy, PostgreSQL, pgvector, Qdrant, Redis

**Production:** Docker, GitHub Actions, CI/CD, typing, testing, secret-safe configuration

---

## How I Build

- Human-in-the-loop for consequential AI actions
- Tests, linting, typing, and build checks as release gates
- Explicit architecture and decision records instead of hidden conventions
- No secrets or private operational data in public repositories
- Demo and local-fallback modes so projects can be evaluated without production credentials
