# SkeinRank

**Open-source infrastructure for governing the language used by search, RAG, and AI agents.**

Teams rarely keep one stable vocabulary. Product names change, aliases accumulate, documentation lags behind code, and independent agents invent different names for the same concept. SkeinRank turns that language into reviewed, versioned, testable infrastructure.

[Website](https://skeinrank.github.io/) · [Main repository](https://github.com/SkeinRank/skeinrank) · [SkeinRank on PyPI](https://pypi.org/project/skeinrank/) · [Agent Lexicon on PyPI](https://pypi.org/project/agent-lexicon/)

## The ecosystem

### Core projects

| Repository | Purpose |
| --- | --- |
| **[skeinrank](https://github.com/SkeinRank/skeinrank)** | Domain Language Control Plane for enterprise search, RAG, and agent workflows. Discover terminology, review evidence, publish versioned dictionaries, and canonicalize runtime text without replacing the search stack you already run. |
| **[agent-lexicon](https://github.com/SkeinRank/agent-lexicon)** | Deterministic shared vocabulary for AI coding agents. Give agents canonical project language before a task, resolve ambiguous terms, guard tool calls, and detect naming drift in diffs and pull requests. |

### Evidence and benchmarks

| Repository | What it demonstrates |
| --- | --- |
| **[skeinrank-benchmark](https://github.com/SkeinRank/skeinrank-benchmark)** | Reproducible cross-version terminology discovery in real open-source documentation. The canonical Airflow 2.7 → 3.0 run reached **P@5 100%** and **P@10 90%** with full label coverage. |
| **[agent-lexicon-benchmark](https://github.com/SkeinRank/agent-lexicon-benchmark)** | Paired AI-agent benchmark over 60 runs. In the reference task set, strict canonical usage increased from **0% to 60%**, while canonical usage inside compound names increased from **10% to 100%**. |
| **[oss-drift-report](https://github.com/SkeinRank/oss-drift-report)** | Reproducible measurements of how long officially renamed terminology survives in projects such as Kubernetes, OpenSearch, Home Assistant, and Airflow. |

### Documentation

| Repository | Purpose |
| --- | --- |
| **[skeinrank.github.io](https://github.com/SkeinRank/skeinrank.github.io)** | Product website, documentation, architecture, and quickstarts for the SkeinRank ecosystem. |

## How the projects fit together

```text
Documents, code, and project terminology
                  │
                  ▼
       SkeinRank discovers and governs
       reviewed, versioned project language
                  │
                  ▼
     Agent Lexicon gives coding agents the
     right vocabulary and checks changes at PR time
                  │
                  ▼
  Benchmarks and drift reports measure the result
```

Use **SkeinRank** when the problem spans search, RAG, documentation, or organization-level terminology governance.

Use **Agent Lexicon** when the immediate problem is keeping coding agents, branches, identifiers, documentation, and tool calls aligned with a project vocabulary.

Use the benchmark and report repositories when you need reproducible evidence rather than a product claim.

## Start locally

### SkeinRank

```bash
pip install skeinrank
```

```python
import skeinrank

skeinrank.canonicalize("k8s pg timeout")
```

### Agent Lexicon

```bash
pipx install agent-lexicon
alex init
alex scan
alex review
alex publish
```

## Design principles

- **Human-reviewed language** — discovery produces candidates; people publish decisions.
- **Deterministic enforcement** — runtime resolution and merge checks can be replayed and audited.
- **Evidence before rollout** — terminology changes carry examples from the content that motivated them.
- **Works beside existing infrastructure** — SkeinRank complements Elasticsearch, OpenSearch, vector databases, CI, and agent tooling rather than replacing them.
- **Measured in public** — benchmark configs, pinned commits, labels, and derived reports live in dedicated repositories.

## Project status

SkeinRank is an actively developed open-source ecosystem. The repositories are usable independently, while sharing one goal: make project language explicit enough to review, version, enforce, and measure.

Start with **[skeinrank](https://github.com/SkeinRank/skeinrank)** for search and governance, or **[agent-lexicon](https://github.com/SkeinRank/agent-lexicon)** for AI coding-agent workflows.
