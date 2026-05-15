# Contributing to APIForge

Thank you for your interest in contributing. All APIForge SDKs are open source under the MIT license and welcome community contributions.

---

## Before you start

- Check if an [issue](https://github.com/APIForge-Organisation/sdk-nodejs/issues) or [discussion](https://github.com/orgs/APIForge-Organisation/discussions) already covers your idea.
- For significant changes, open an issue first to align on the approach before writing code.
- For small fixes (typos, docs, obvious bugs), feel free to open a PR directly.

---

## Branch model

All repositories follow the same branching strategy:

| Branch | Purpose |
|---|---|
| `main` | Production — protected, only merged via PR |
| `dev` | Integration — base branch for all development |
| `feat/<name>` | New features |
| `fix/<name>` | Bug fixes |
| `docs/<name>` | Documentation only |

**Always branch from `dev`, and target `dev` in your PR.** The maintainers handle `dev → main` merges for releases.

---

## Development workflow

### 1. Fork and clone

```bash
git clone https://github.com/<your-username>/<repository>.git
cd <repository>
git checkout dev
git checkout -b feat/your-feature-name
```

### 2. Install dependencies

```bash
npm install        # Node.js repos
# or
pip install -e ".[dev]"   # Python repos
```

### 3. Make your changes

- Keep changes focused — one PR, one concern.
- Follow the existing code style (ESLint / Prettier configs are included).
- Write or update tests for any changed behavior.

### 4. Run tests

```bash
npm test           # Node.js
pytest             # Python
```

All tests must pass before opening a PR.

### 5. Commit and push

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add sampling rate config option
fix: handle undefined route in interceptor
docs: update quick start example
chore: bump node version in CI
```

### 6. Open a Pull Request

Target the `dev` branch. Fill in the PR template completely — especially the testing section.

---

## Code standards

**Node.js repositories:**
- Node.js 22+ required
- ESLint with the project config — run `npm run lint` before pushing
- No new dependencies without prior discussion (keep the SDK lightweight)

**All repositories:**
- No sensitive data in code or commits (API keys, tokens, real URLs, private IPs)
- Privacy-first: the SDK must never capture request/response bodies, headers, or user-identifying data
- Performance matters: changes to the hot path (interceptor, aggregator) must include benchmark notes

---

## Reporting a vulnerability

Do **not** open a public issue for security vulnerabilities. See [SECURITY.md](SECURITY.md).

---

## Questions?

Open a [Discussion](https://github.com/orgs/APIForge-Organisation/discussions) — we're happy to help.
