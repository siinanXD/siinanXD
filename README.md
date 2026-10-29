# Hi, I'm Sinan

**AI Engineer with an industrial background.** Trained and worked as an electronics technician for industrial systems (Elektroniker für Betriebstechnik, 2012–2023) before moving into AI engineering in 2024. I build AI systems for the shop floor: maintenance assistants, document intelligence for machine manuals and electrical drawings, and agents that act on real operational data with a human in the loop.

Euskirchen, Germany · [LinkedIn](https://www.linkedin.com/in/kahraman-sinan/) · [sjcode.de](https://sjcode.de)

---

## Featured Projects

### [Stromlauf AI](https://github.com/siinanXD/stromlauf-ai) · [Live demo](https://stromlauf-ai.vercel.app)
[![CI](https://github.com/siinanXD/stromlauf-ai/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/stromlauf-ai/actions/workflows/ci.yml)

Chat over the electrical documentation of a machine: circuit diagrams (PDF, including scans via OCR), terminal plans, parts lists, Siemens STEP 7 AWL/SCL. Every answer cites its source (`[[file|location]]`); signal paths, fault cards and gap lists are computed deterministically without a model call. Ingest, plan-graph and retrieval gates run in CI with fixed thresholds; a weekly paid agent run measures facts, sources and citation validity on a gold set. Demo mode with a sample machine, no uploads, rate-limited.

> Python · FastAPI · LangGraph · Docling · RapidOCR · PostgreSQL/pgvector · Next.js · TypeScript · Playwright · Langfuse

### [Content-Agent-Lernapp](https://github.com/siinanXD/Content-Agent-Lernapp) · [Live](https://content-agent-ashen-nu.vercel.app)
[![ci](https://github.com/siinanXD/Content-Agent-Lernapp/actions/workflows/ci.yml/badge.svg)](https://github.com/siinanXD/Content-Agent-Lernapp/actions/workflows/ci.yml)

Learning app for German vocational training that generates courses from official sources (training regulations, framework curricula). A generator model writes questions, a second model judges them against fixed criteria, and only passing content is published; a human approves. Learning path, spaced repetition, exams, trainer groups with invitation links. Supabase with row-level security, nightly backups with a monthly restore test, Playwright and axe checks on every route, Langfuse traces per unit.

> Next.js · TypeScript · Supabase/PostgreSQL · Claude Batch API · OpenAI · Playwright · Langfuse · Sentry · PostHog

### [Leitstand](https://github.com/siinanXD/Leitstand) (archived, read-only)

Control plane that ran my repositories autonomously: tasks from Linear, a dispatcher, a second-model reviewer, repair loops, merge gates and a daily note into an Obsidian vault. Replaced in October 2026 by a much smaller setup on top of T3 Code (private). Kept public as a record of what worked and what did not.

> TypeScript · Next.js · Supabase · GitHub Actions

Earlier projects, archived and read-only: [Maintenance AI Assistant](https://github.com/siinanXD/maintenance-ai-assistant) (industrial maintenance with work orders, inspections and a tool-using assistant) · [Document Intelligence MVP](https://github.com/siinanXD/document-intelligence-mvp) (multi-tenant RAG over technical documents with grounded citations) · [Mail Agent](https://github.com/siinanXD/Mail-agent) (IMAP agent for vacation-rental mailboxes) · [Agent Eval Harness](https://github.com/siinanXD/agent-eval-harness) · [Online Lerncampus](https://github.com/siinanXD/Online-Lerncampus) · [sjcode.de](https://github.com/siinanXD/SJCODE-website) (this site's source)

---

## Current Direction: AI for Industry 4.0

I am building AI applications for manufacturing and the German Mittelstand, where I know the domain from the inside:

- **Electrical documentation assistant** ([Stromlauf AI](https://github.com/siinanXD/stromlauf-ai), live demo above): a chatbot over circuit diagrams, terminal plans, parts lists and Siemens STEP 7 AWL programs that tracks devices (`-K12`), terminals (`-X1:5`) and PLC addresses (`E0.0`) across all documents
- **Maintenance and inspection workflows** with legal proof (DGUV V3, BetrSichV) and a human approval step before anything is written
- **Grounded RAG over machine manuals** with citations, measurable retrieval quality and "the documents do not say" as an honest answer

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
