<p align="center">
  <a href="https://skeinrank.github.io">
    <img src="https://skeinrank.github.io/skeinrank-favicon.png" alt="SkeinRank logo" width="88" height="88" />
  </a>
</p>

<h1 align="center">SkeinRank</h1>

<p align="center">
  <strong>Open-source terminology control plane for search and RAG.</strong>
</p>

<p align="center">
  <a href="https://github.com/SkeinRank/skeinrank/actions/workflows/ci.yml">
    <img alt="CI" src="https://github.com/SkeinRank/skeinrank/actions/workflows/ci.yml/badge.svg" />
  </a>
  <a href="https://pypi.org/project/skeinrank/">
    <img alt="PyPI" src="https://img.shields.io/pypi/v/skeinrank.svg" />
  </a>
  <a href="https://github.com/SkeinRank/skeinrank/blob/main/LICENSE">
    <img alt="License" src="https://img.shields.io/github/license/SkeinRank/skeinrank.svg" />
  </a>
  <a href="https://skeinrank.github.io">
    <img alt="Website" src="https://img.shields.io/badge/website-skeinrank.github.io-22d3ee" />
  </a>
</p>

<p align="center">
  <a href="https://skeinrank.github.io">Website</a> ·
  <a href="https://skeinrank.github.io/getting-started/quickstart/">Quickstart</a> ·
  <a href="https://skeinrank.github.io/platform-preview/">Platform Preview</a> ·
  <a href="https://github.com/SkeinRank/skeinrank">Main repository</a>
</p>

---

SkeinRank helps teams turn messy aliases, internal jargon, and domain-specific terminology into governed runtime context for enterprise search, Elasticsearch enrichment, RAG, and knowledge workflows.

Instead of treating terms like `k8s`, `kube`, `postgres`, `pg`, or internal project aliases as loose text, SkeinRank lets teams normalize them into canonical concepts, review evidence, publish snapshots, and serve stable context to downstream search and AI systems.

## What SkeinRank is building

- **Terminology governance** for canonical terms, aliases, profiles, bindings, and snapshots.
- **Search enrichment workflows** for technical documents, incidents, runbooks, and enterprise knowledge bases.
- **Runtime context APIs** that help search, RAG, and agent systems use governed terminology safely.
- **Evidence-assisted review** so teams can validate terminology changes against real indexed content.

## Main repository

| Repository | Purpose |
| --- | --- |
| [`SkeinRank/skeinrank`](https://github.com/SkeinRank/skeinrank) | Main monorepo with the core library, governance API, UI, Elasticsearch workflows, Docker Compose stack, and documentation. |

## Project status

SkeinRank is in active public preview. The current focus is on the terminology control plane, Docker Compose deployment path, governance console, Elasticsearch evidence workflows, and search/RAG integration surfaces.

For the product overview and docs, start at **[skeinrank.github.io](https://skeinrank.github.io)**.
