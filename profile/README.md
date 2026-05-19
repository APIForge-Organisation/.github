<div align="center">
  <h1>APIForge</h1>
  <p><strong>API Intelligence & Observability Platform</strong></p>
  <p>Understand your APIs. Detect drifts. Ship with confidence.</p>

  <p>
    <a href="https://apiforge-organisation.github.io/docs/"><img src="https://img.shields.io/badge/docs-online-0066FF" alt="Documentation"></a>
    <a href="https://www.npmjs.com/package/apiforgejs"><img src="https://img.shields.io/npm/v/apiforgejs?label=sdk-nodejs&color=0066FF" alt="npm version"></a>
    <a href="https://pypi.org/project/apiforgepy/"><img src="https://img.shields.io/pypi/v/apiforgepy?label=sdk-python&color=0066FF" alt="PyPI version"></a>
    <a href="https://github.com/APIForge-Organisation/sdk-nodejs/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="License MIT"></a>
    <a href="https://github.com/APIForge-Organisation/sdk-nodejs/actions"><img src="https://img.shields.io/github/actions/workflow/status/APIForge-Organisation/sdk-nodejs/ci.yml?branch=main&label=CI%20Node.js" alt="CI Node.js"></a>
    <a href="https://github.com/APIForge-Organisation/sdk-python/actions"><img src="https://img.shields.io/github/actions/workflow/status/APIForge-Organisation/sdk-python/ci.yml?branch=main&label=CI%20Python" alt="CI Python"></a>
  </p>
</div>

---

## What is APIForge?

APIForge is a **behavioral intelligence and observability platform** specialized for backend APIs.

Unlike generic monitoring tools, APIForge doesn't just display raw metrics — it **understands how your APIs behave over time**: detecting drifts, correlating releases with incidents, and proactively surfacing anomalies.

> *"APIForge doesn't just measure an API. It understands its behavior over time."*

---

## Three core principles

**Privacy-first** — No sensitive data ever leaves your environment. The SDK captures only anonymized technical metadata: route patterns (never real values), latency, status codes.

**Local-first** — Works completely offline. No account required, no cloud configuration. Just `npm install` and one line of code.

**Developer-first** — Up and running in under 5 minutes. Zero mandatory configuration.

---

## Quick start

**Node.js (Express)**

```bash
npm install apiforgejs
```

```javascript
const { apiforge } = require('apiforgejs');

app.use(apiforge({ mode: 'local' }));

// Dashboard → http://localhost:4242
```

**Python (FastAPI / Starlette)**

```bash
pip install apiforgepy
```

```python
from fastapi import FastAPI
from apiforgepy import ApiForgeMiddleware

app = FastAPI()
app.add_middleware(ApiForgeMiddleware, mode="local")

# Dashboard → http://localhost:4242
```

That's it. Your API dashboard is live.

**→ [Full documentation](https://apiforge-organisation.github.io/docs/)**

---

## What you get out of the box

| Feature | Description |
|---|---|
| **P50 / P90 / P99 latency** | Per-endpoint percentile tracking |
| **Error rate by route** | Real-time 2xx / 4xx / 5xx breakdown |
| **API Health Score** | Single 0–100 score summarizing your API health |
| **Automatic insights** | Plain-language alerts — no dashboard configuration needed |
| **Dead endpoint detection** | Identifies routes with no traffic in the last 21 days |
| **Release impact tracking** | Before/after comparison on every deploy |
| **Drift detection** | OLS regression over 30 days — catches slow degradations invisible day-to-day |
| **Bandwidth tracking** | Average response size per route (`bytes_avg`) via `Content-Length` |

---

## Repositories

| Repository | Description | Status |
|---|---|---|
| [sdk-nodejs](https://github.com/APIForge-Organisation/sdk-nodejs) | Express.js SDK — local-first observability middleware | `Active` |
| [sdk-python](https://github.com/APIForge-Organisation/sdk-python) | FastAPI / Starlette SDK — local-first observability middleware | `MVP` |
| [docs](https://github.com/APIForge-Organisation/docs) | Documentation — [apiforge-organisation.github.io/docs](https://apiforge-organisation.github.io/docs/) | `Live` |
| [sdk-nestjs](https://github.com/APIForge-Organisation/sdk-nestjs) | NestJS SDK | `Planned` |
| [api](https://github.com/APIForge-Organisation/api) | SaaS backend — Express.js + Prisma + BullMQ | `In Progress` |
| [dashboard](https://github.com/APIForge-Organisation/dashboard) | React SaaS dashboard — React 19 + TypeScript + Tailwind | `In Progress` |

---

## Roadmap

- [x] **Phase 1 — MVP Local** · Express.js SDK · SQLite · Dashboard on port 4242 · Insights (anomaly, dead endpoints, drift detection, release impact)
- [ ] **Phase 2 — Multi-SDK** · FastAPI ✅ · NestJS · Universal event protocol
- [ ] **Phase 3 — SaaS** · Cloud collector · PostgreSQL + TimescaleDB · Pro & Team plans *(in development)*
- [ ] **Phase 4 — Advanced Intelligence** · ML anomaly detection · Multi-service correlation · Weekly reports

---

## Contributing

All SDKs are open source under the MIT license. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

Found a bug? [Open an issue](https://github.com/APIForge-Organisation/sdk-nodejs/issues/new/choose).  
Have an idea? [Start a discussion](https://github.com/orgs/APIForge-Organisation/discussions).

---

<div align="center">
  <sub>Built with care · Privacy-first · Local-first · Developer-first</sub>
</div>
