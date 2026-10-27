# Support Agent

A customer support agent for a fake online store, built step by step: from a basic LLM call to a deployed, tested, production-ready agent.

Each step improves the same system, and each step is documented in `docs/` with what I built, the tools I used, the edge cases I tested, and what broke along the way.

## Status

🚧 Step 1 in progress

## Roadmap

- [ ] **Step 1: Basic model app**: a reliable LLM call with retries, error handling, and logging
- [ ] **Step 2: Retrieval**: answers grounded in the store's help docs, with citations
- [ ] **Step 3: Tools**: order lookup and refunds, with permissions and human approval
- [ ] **Step 4: State and memory**: tickets and history stored in PostgreSQL
- [ ] **Step 5: Durable workflows**: multi-step flows that pause, resume, and recover
- [ ] **Step 6: Evals and observability**: a test set, metrics, and tracing
- [ ] **Step 7: Production**: API, auth, Docker, CI, monitoring, and deployment
- [ ] **Step 8: Final polish**: architecture docs, eval results, and failure traces

## Setup

Requires [uv](https://docs.astral.sh/uv/).

```bash
git clone https://github.com/Epciy/support-agent.git
cd support-agent
uv sync
cp .env.example .env   # then add your Anthropic API key
uv run support-agent
```

## Tech stack

- Python 3.12
- uv
- Anthropic SDK
- pydantic-settings, tenacity, structlog
- pytest
