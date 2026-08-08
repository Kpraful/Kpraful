# Hey, I'm Praful 👋

> I build LLM systems that survive production.

```python
praful = {
    "role":      "AI Software Engineer @ BCG X",
    "based_in":  "Delhi NCR, India",
    "years":     4,
    "building":  ["agent harnesses", "RAG that cites", "multi-tenant platforms"],
    "stack":     ["Python", "FastAPI", "Azure", "Postgres", "pgvector"],
    "belief":    "an agent that fails loudly beats an agent that guesses quietly",
    "debugging": "why it called the same tool six times",
}
```

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![LangChain](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)

---

## 🧠 What I actually build

Four things I have shipped to real tenants. Click any of them if you want the guts.

<details>
<summary><b>🔌 Agentic AI, and a 39-tool MCP server</b></summary>

<br>

Built the natural-language layer of an enterprise platform: a **39-tool MCP server** on FastMCP, exposing internal tools and data to LLM agents over Claude and Gemini.

- Tenant resolved from the authenticated Okta identity, **never** from caller input. 403 invariant on every cross-tenant request, with a security suite that proves it.
- Patched the tool decorator once so all 39 tools auto-wrap with error boundaries, correlation IDs and structured audit logs. Zero per-tool boilerplate.
- Guardrails that forbid the model from stating any number a tool did not return. No fine-tuning, no hallucinated market figures.
- Hand-rolled agent control loop: bounded 6-step tool calling, explicit stopping criterion, exceptions fed back as tool messages so the model recovers instead of crashing.

</details>

<details>
<summary><b>🔍 Retrieval that holds up under questioning</b></summary>

<br>

- Hybrid search fusing **pgvector** semantic retrieval with Postgres full-text via **Reciprocal Rank Fusion**, configurable 70/30 weighting plus document-type weighting.
- Multi-query expansion, token-by-token streaming, conversation memory, page-level citation extraction, all inside a 128K token budget.
- Document-type-aware recursive chunking with sentence-window and metadata enrichment into 1536-dimension embeddings.
- A vision path for presentations, then hierarchical DBSCAN clustering of embeddings into trend clusters with LLM-written summaries.

</details>

<details>
<summary><b>⚙️ LLM-Ops, the unglamorous half</b></summary>

<br>

- Per-tenant multi-provider routing across OpenAI, Azure OpenAI and Gemini, with **time-to-first-token fallback that re-routes mid-stream**, a circuit breaker, and per-user and per-tenant inflight limits.
- **165+ versioned prompts** resolved per-tenant-override then common-default, cached in Redis with hot reload, so subject-matter experts ship prompt changes without a redeploy.
- Every call traced in LangSmith and correlated into Datadog APM, with tiktoken cost accounting and per-provider context-window management.
- An LLM benchmarking harness scoring models on five quality dimensions plus latency, TTFT, throughput and cost, used to actually pick models.

</details>

<details>
<summary><b>🏗️ The platform underneath all of it</b></summary>

<br>

- Multi-tenant Azure self-service platform: app architecture, networking, Kubernetes, Container Apps Jobs. **10+ tenants, 10,000+ users.**
- Per-tenant database isolation with encrypted connection strings, lazily created and dynamically budgeted pools, and ContextVar tenant propagation across async tasks. New tenants need no restart.
- Okta OIDC with spoof-proof group-to-tenant mapping, role-based endpoint guards, and JWT auto-refresh that never forces a re-login.
- **Terraform**: six reusable Azure modules standing up an isolated subscription per client, VNet, database and storage included, in about 30 minutes.

</details>

---

## 📊 Receipts

Numbers I can defend in an interview.

| What I built | What it moved |
| :--- | :--- |
| 🏢 Multi-tenant Azure platform | 10+ tenants, 10,000+ users, up to 5 clients per server |
| ⚡ Onboarding automation | 7-10 days ➜ **1-2 hours**, and 6-month infra cost per client from $6,000 ➜ **$1,200-$2,000** |
| 📄 Event-driven RAG pipeline | 50-100 docs per client, turnaround from weeks ➜ **hours** |
| 🩺 LLM upload diagnostics agent | Catches **~90%** of errors pre-processing, debugging days ➜ minutes, answers in **under 90s** |
| 🎯 GenAI synthetic survey panel | Redesigned probabilistic aggregation, prediction error **47pt ➜ 10pt** vs real respondents |
| 🧮 Synthetic panel modeling core | Seeded k-means++ over 54-dim vectors, ~6,000 respondents ➜ ~250-300 prototypes, **~20x** cheaper per question |
| 🐘 Backend perf work (Infosys) | Query optimization and pooling, latency down **up to 30%** |

---

## 🧰 Toolbox

**GenAI and LLM**

![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%20%2F%20FastMCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain%20%2F%20LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20%2B%20Embeddings-FF6F00?style=flat-square)
![Agents](https://img.shields.io/badge/Agentic%20Tool--Use-6E56CF?style=flat-square)

**Backend**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)

**Cloud and DevOps**

![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Redux](https://img.shields.io/badge/Redux%20Toolkit-764ABC?style=flat-square&logo=redux&logoColor=white)

---

## 🏅 Badges that came with an exam

- 🎖️ Microsoft Certified: **Azure Administrator Associate (AZ-104)** and **Azure Fundamentals (AZ-900)**
- 🇮🇳 **National Finalist**, Smart India Hackathon 2020
- 🧩 Top **27%** on LeetCode, **300+** problems solved
- 🎓 **B.E. Computer Engineering**, Bharati Vidyapeeth College of Engineering, Pune. CGPA 8.63

---

## ☕ Off the clock

- 🔬 Reading eval papers, then arguing with the benchmark
- 🏗️ Rebuilding things that already work, but slower and with more logging
- 🧠 Convinced that most "the model is bad" bugs are actually retrieval bugs
- 🏆 Recovering hackathon person, still gets the itch every October

---

## 📫 Find me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://in.linkedin.com/in/prafulkatare)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:prafulkatare6@gmail.com)

Always up for a conversation about agent infrastructure, retrieval, or why your LLM pipeline is slow. 🚀
