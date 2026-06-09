<p align="center">
  <a href="https://skeinrank.github.io">
    <img src="https://skeinrank.github.io/skeinrank-favicon.png" alt="SkeinRank logo" width="88" height="88" />
  </a>
</p>

<h1 align="center">SkeinRank</h1>

<p align="center">
  <strong>The open-source control plane for the language your search runs on.</strong>
</p>

<p align="center">
  Your team's vocabulary drifts — features get renamed, slang piles up, acronyms collide.<br/>
  Your embedding model never learned your internal names, so retrieval quietly rots.<br/>
  SkeinRank detects that drift, versions your terminology, and keeps search quality under control as you scale.
</p>

<p align="center">
  <a href="https://skeinrank.github.io">Website</a> ·
  <a href="https://skeinrank.github.io/getting-started/quickstart/">Quickstart</a> ·
  <a href="https://skeinrank.github.io/docs/">Docs</a> ·
  <a href="https://github.com/SkeinRank/skeinrank">Main repo</a> ·
  <a href="https://pypi.org/project/skeinrank/">PyPI</a>
</p>

<p align="center">
  <a href="https://github.com/SkeinRank/skeinrank/actions/workflows/ci.yml">
    <img alt="CI" src="https://github.com/SkeinRank/skeinrank/actions/workflows/ci.yml/badge.svg" />
  </a>
  <a href="https://pypi.org/project/skeinrank/">
    <img alt="PyPI" src="https://img.shields.io/pypi/v/skeinrank?color=8b5cf6" />
  </a>
  <a href="https://github.com/SkeinRank/skeinrank/blob/main/LICENSE">
    <img alt="License" src="https://img.shields.io/github/license/SkeinRank/skeinrank?color=22d3ee" />
  </a>
</p>

---

## The problem nobody is measuring

Retrieval quality isn't static — it decays.

A feature called `checkout-v2` in January becomes `payments-core` in your June docs. On-call still types "the checkout thing." Three names for one reality, indexed at different times. Your embedding model never saw your internal names on the public internet, so it guesses — and as your language drifts, those guesses rot. No error, no alert, just search that's a little worse every month until someone says *"the bot got dumb."*

Your vocabulary is the one input to retrieval that changes constantly — and no system owns it, versions it, or tells you when it drifts.

**SkeinRank is that system.**

## What SkeinRank does

A terminology **control plane** that sits beside the Elasticsearch, OpenSearch, or vector DB you already run. It doesn't replace your search engine — it governs the language feeding into it.

- **Drift detection** — measure how far your live language has moved from the vocabulary your search relies on.
- **Terminology governance** — canonical terms, aliases, profiles, bindings, and immutable versioned snapshots.
- **Context-aware disambiguation** — `pg timeout` resolves differently from `pg layout`, by explicit rule, not a guess.
- **Evidence-assisted review** — validate every change against real indexed content before it ships.
- **Safe rollout** — blue/green alias swap, rollback, and before/after retrieval evaluation.
- **Agent integration via MCP** — agents can *propose* terminology fixes under strict RBAC, but never mutate production directly.

## Try it in 60 seconds

```bash
pip install skeinrank
```

```python
import skeinrank
skeinrank.canonicalize("k8s pg timeout")   # → "kubernetes postgresql timeout"
skeinrank.canonicalize("pg layout")        # → "page layout"
```

## Repositories

| Repository | What's inside |
| --- | --- |
| **[skeinrank](https://github.com/SkeinRank/skeinrank)** | Monorepo: Python SDK & CLI, governance API, React console, Elasticsearch provider, Helm chart, Docker Compose stack, and docs. |

Inside the monorepo:

| Package | Purpose |
| --- | --- |
| `skeinrank-core` | Python SDK, CLI, canonicalization & extraction |
| `skeinrank-governance-api` | FastAPI control-plane API, workers, MCP adapter |
| `skeinrank-provider-elasticsearch` | Elasticsearch provider & enrichment CLI |
| `skeinrank-ui` | React/TypeScript governance console |

## Project status

SkeinRank is in active open-source public preview — not a hosted SaaS. Current focus: binding-aware runtime canonicalization, terminology drift detection, safe governance, Terminology-as-Code, and operator-controlled Elasticsearch/OpenSearch delivery.

Start at **[skeinrank.github.io](https://skeinrank.github.io)** · Apache-2.0 licensed.