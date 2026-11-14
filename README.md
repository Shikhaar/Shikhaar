# Hi, I'm Shikhar Srivastava

**AI/ML engineer. I build AI products end to end: the agents, the retrieval, and the infrastructure behind them.**

`Agentic systems` · `Retrieval` · `AI observability` · `Production engineering`

<p align="left">
  <a href="https://linkedin.com/in/shikhar004">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://leetcode.com/u/Shikhar3004">
    <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode" />
  </a>
  <a href="https://shikhar-portfolio-phi.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
  <a href="mailto:shikharsrivastava3004@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

---

## How I build

- **LLMs interpret, code decides.** Scores, dependency graphs and costs are computed deterministically, so the result is reproducible and auditable. The model explains the result and writes the content.
- **Small agents over one big prompt.** Each step has its own inputs, outputs and failure modes, so it can be tested, retried and observed on its own.
- **Measure, don't trust.** I check against ground truth: real provider bills, network traffic and test results, never the model's own report.
- **Keep AI out of the critical path.** Expensive or uncertain work runs async, behind a fallback, or waits for human approval.

---

## Projects

### [TestPilot AI](https://github.com/Shikhaar/TestPilot-AI)

Autonomous regression testing. On every PR it finds the affected code paths with AST-based dependency analysis (Tree-sitter), generates targeted tests, runs them in a sandbox, diagnoses failures and posts a review.

<img src="https://raw.githubusercontent.com/Shikhaar/TestPilot-AI/HEAD/docs/images/dashboard.png" alt="TestPilot AI dashboard" width="720" />

- **11 LangGraph agents** with parallel fan-out, fed by 3-layer hybrid retrieval (dense + keyword + disk scan)
- **32% fewer prompt tokens** from AST-based context pruning, with no drop in test pass rate
- **4 test frameworks and 4 git hosts**, with Pass@1/Pass@N, repair rate and token cost tracked on every run

`Python` `FastAPI` `LangGraph` `Tree-sitter` `Qdrant` `PostgreSQL` `Celery` `Redis` `Next.js`

### [BrandBrew: Content Copilot](https://github.com/Shikhaar/Helium-Content-Copilot) · [Live demo](https://helium-content-copilot.onrender.com)

AI content strategist for D2C brands. It decides what is worth making before it writes anything, then drafts platform-ready posts for a human to approve and schedule.

- **Deterministic 100-point score** across 5 signals. The LLM explains the score but never sets it.
- **Zero image-generation cost per draft** (vs $0.08–$0.20 for generated images), because it uses the brand's real catalog photos with AI-written copy on top
- **Structured generation** with GPT-4o-mini, CO-STAR prompting and validated JSON output, with a fallback when the LLM is unavailable

`Python` `FastAPI` `OpenAI` `Pydantic` `Next.js` `TypeScript` `Clerk`

### [Burnrate](https://github.com/Shikhaar/burnrate)

LLM spend tracking. It attributes every AI dollar to a project, feature, team or customer, and checks its estimates against what providers actually bill.

- **OpenAI, Anthropic, Google and Mistral**, plus coding-agent spend from Claude Code, Cursor and Copilot
- **Billing reconciliation** against the OpenAI and Anthropic cost APIs, flagging any provider whose real bill drifts from the token-based estimate
- **Forecasting and anomaly detection** (robust median/MAD z-scores), with Slack and Jira alerts
- **Python and TypeScript SDKs** plus an OpenTelemetry receiver, so nothing sits in the request path

`Python` `FastAPI` `PostgreSQL` `Redis` `OpenTelemetry` `Next.js` `Docker`

### Also built

- **[HarnessBench](https://github.com/Shikhaar/HarnessBench)**: benchmarks coding-agent harnesses (Claude Code, Aider) with the LLM held constant, measuring cost through a wire-level proxy
- **[RAG from Scratch](https://github.com/Shikhaar/Rag-from-Scratch)**: BM25, dense search, rank fusion and reranking with no frameworks. Hybrid search reaches 1.00 Recall@5, vs 0.94 for either retriever alone.
- **[AI Factory](https://github.com/Shikhaar/AI-Factory)**: a multi-agent team (architect, backend, frontend, QA) that builds full-stack apps, coordinated by a deterministic state machine instead of agents talking to each other

---

## Tools I use

- **Languages:** Python · TypeScript · SQL
- **AI & orchestration:** LangGraph · LiteLLM · Instructor · OpenAI / Anthropic APIs · PyTorch · Hugging Face
- **Retrieval:** Qdrant · Hybrid search (dense + BM25) · Cross-encoder reranking
- **Backend & infrastructure:** FastAPI · Celery · Redis · PostgreSQL · Docker
- **Observability:** OpenTelemetry · Prometheus · Grafana
