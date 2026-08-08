# Praful Katare

**AI Software Engineer at BCG X** | GenAI and agentic systems, multi-tenant backend platforms

I build LLM systems that survive production: agent harnesses with real stopping criteria, RAG that cites its sources, and the multi-tenant Azure platforms underneath them. 4+ years total, the last of them shipping GenAI to 10+ enterprise tenants and 10,000+ users.

Based in Delhi NCR, India.

---

## What I work on

**Agentic AI.** A 39-tool MCP server (FastMCP) that exposes internal tools and data to LLM agents over Claude and Gemini, with server-side tenant isolation resolved from the authenticated identity rather than caller input, a 403 invariant on every cross-tenant call, and guardrails that stop the model stating any number a tool did not return.

**Retrieval that holds up.** Hybrid search fusing pgvector semantic retrieval with Postgres full-text via Reciprocal Rank Fusion, document-type weighting, multi-query expansion, page-level citations, and streaming answers under a 128K token budget.

**LLM-Ops.** Per-tenant multi-provider routing across OpenAI, Azure OpenAI and Gemini with time-to-first-token fallback that re-routes mid-stream, circuit breakers, inflight limits, 165+ versioned prompts hot-reloaded from blob storage through Redis, and every call traced in LangSmith and Datadog with token and cost accounting.

**Backend and platform.** Per-tenant database isolation with encrypted connection strings and dynamically budgeted pools, Okta OIDC with group-to-tenant mapping, Terraform modules that stand up an isolated Azure subscription per client in about 30 minutes, and an event-driven document pipeline on Azure Queue Storage.

---

## Selected results

| What | Impact |
| --- | --- |
| Multi-tenant Azure self-service platform | 10+ tenants, 10,000+ users, up to 5 clients per server |
| Client onboarding automation | 7-10 days down to 1-2 hours; 6-month infra cost per client from $6,000 to $1,200-$2,000 |
| Event-driven RAG and embedding pipeline | 50-100 documents per client, turnaround from weeks to hours |
| LLM upload diagnostics agent | Catches ~90% of upload errors pre-processing, debugging from days to minutes, results under 90 seconds |
| GenAI synthetic survey panel | Redesigned probabilistic aggregation, prediction error from 47pt to 10pt against real respondents |
| Synthetic panel modeling core | Seeded k-means++ over 54-dimensional feature vectors, ~6,000 respondents compressed to ~250-300 prototypes, ~20x lower LLM cost per question |
| Backend performance work (Infosys) | Query optimization and connection pooling, latency down up to 30% |

---

## Tech I use in production

**GenAI and LLM**
LLM engineering, RAG, OpenAI API, structured outputs, Model Context Protocol (MCP), FastMCP, agentic tool-use, multi-agent orchestration, LangChain, LangGraph, prompt engineering, embeddings, pgvector, vector search, LLM evaluation and benchmarking

**Backend and architecture**
Python, FastAPI, Flask, Django, Node.js, REST API design, event-driven systems, multi-tenant architecture, microservices, observability

**Cloud and DevOps**
Microsoft Azure, AKS, Azure Container Apps, Azure Functions, Azure Queue Storage, Docker, Kubernetes, Helm, Terraform, GitHub Actions, CI/CD

**Data**
PostgreSQL, pgvector, MongoDB, Snowflake, SQL, pandas, NumPy, scikit-learn

**Frontend**
React 19, TypeScript, Vite, Redux Toolkit, TanStack Query, Chart.js

---

## Certifications and achievements

- Microsoft Certified: **Azure Administrator Associate (AZ-104)** and **Azure Fundamentals (AZ-900)**
- **National Finalist**, Smart India Hackathon 2020
- Top **27%** on LeetCode, **300+** DSA problems solved

---

## Education

**B.E., Computer Engineering** | Bharati Vidyapeeth College of Engineering, Pune
2018 to 2022, CGPA 8.63

---

## Connect

- Email: prafulkatare6@gmail.com
- LinkedIn: [in.linkedin.com/in/prafulkatare](https://in.linkedin.com/in/prafulkatare)

Open to conversations about AI engineering, agent infrastructure, and backend platform work.
