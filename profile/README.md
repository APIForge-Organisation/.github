<div align="center">
  <h1>APIForge</h1>
  <p><strong>API Intelligence & Observability Platform</strong></p>
  <p>Understand your APIs. Detect drifts. Ship with confidence.</p>

  <p>
    <a href="https://apiforge-organisation.github.io/docs/"><img src="https://img.shields.io/badge/docs-online-0066FF" alt="Documentation"></a>
    <a href="https://www.npmjs.com/package/apiforgejs"><img src="https://img.shields.io/npm/v/apiforgejs?label=sdk-nodejs&color=0066FF" alt="npm version"></a>
    <a href="https://github.com/APIForge-Organisation/sdk-nodejs/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="License MIT"></a>
    <a href="https://github.com/APIForge-Organisation/sdk-nodejs/actions"><img src="https://img.shields.io/github/actions/workflow/status/APIForge-Organisation/sdk-nodejs/ci.yml?branch=main&label=CI" alt="CI"></a>
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

```bash
npm install apiforgejs
```

```javascript
const { apiforge } = require('apiforgejs');

// Drop this anywhere in your Express app
app.use(apiforge({ mode: 'local' }));

// Dashboard → http://localhost:4242
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
| **Drift detection** | Catches slow degradations invisible day-to-day |

---

## Repositories

| Repository | Description | Status |
|---|---|---|
| [sdk-nodejs](https://github.com/APIForge-Organisation/sdk-nodejs) | Express.js SDK — local-first observability middleware | `MVP` |
| [docs](https://github.com/APIForge-Organisation/docs) | Documentation — [apiforge-organisation.github.io/docs](https://apiforge-organisation.github.io/docs/) | `Live` |
| [sdk-python](https://github.com/APIForge-Organisation/sdk-python) | FastAPI / Django SDK | `Planned` |
| [sdk-nestjs](https://github.com/APIForge-Organisation/sdk-nestjs) | NestJS SDK | `Planned` |
| [api](https://github.com/APIForge-Organisation/api) | SaaS backend — collector, engine, auth | `Planned` |
| [dashboard](https://github.com/APIForge-Organisation/dashboard) | React SaaS dashboard | `Planned` |

---

## Roadmap

- [x] **Phase 1 — MVP Local** · Express.js SDK · SQLite · Dashboard on port 4242 · Insights (anomaly, dead endpoints, release impact)
- [ ] **Phase 2 — Multi-SDK** · FastAPI · NestJS · Universal event protocol
- [ ] **Phase 3 — SaaS** · Cloud collector · PostgreSQL + TimescaleDB · Pro & Team plans
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
