# SkeinRank

SkeinRank is an open-source toolkit for explainable terminology normalization and attribute enrichment for technical documents, incidents, and search indexes.

It helps teams map internal jargon, aliases, and domain-specific terms to canonical technical attributes that can be used for search, filtering, reranking, analytics, and governance.

## What SkeinRank does

- Normalizes aliases such as `k8s`, `kube`, and `kuber` into canonical entities like `kubernetes`.
- Extracts typed attributes from technical text, such as `TOOL`, `DB`, `COMPONENT`, `ERROR`, `VERSION`, and `ENVIRONMENT`.
- Groups canonical values by slots, so search systems can distinguish tools, databases, components, errors, versions, and environments.
- Produces explainable passport/debug output showing what was matched, accepted, filtered, or normalized.
- Enriches JSONL datasets and Elasticsearch indexes with compact search-friendly metadata.
- Supports custom terminology profiles, profile validation, and snapshot-based runtime configuration.
- Provides a governance foundation for managing profiles, canonical terms, aliases, and snapshots.

## Repository

- [skeinrank](https://github.com/SkeinRank/skeinrank) — main monorepo with core, server, Elasticsearch provider, and governance package.

## Current focus

SkeinRank is currently focused on:

- terminology normalization
- technical search enrichment
- Elasticsearch enrichment
- profile validation
- governance workflows
- snapshot-based runtime architecture

## Status

SkeinRank is in early active development.