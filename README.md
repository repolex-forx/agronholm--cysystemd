# Repolex Knowledge Graph of agronholm/cysystemd

RDF knowledge graph data for [agronholm/cysystemd](https://github.com/agronholm/cysystemd), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download agronholm/cysystemd
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aa82d02de61b7c9257853da4fc85f156c55d85ea
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── aa82d02de61b7c9257853da4fc85f156c55d85ea
│           └── chunk-001.nq.gz
├── blob
│   ├── 15908ade29ea0d6b27ab1b7a0df1088304dc82ae.nq.gz
│   ├── 18ad5afdc9bc5be35f0c21ba08331b7659f6ba03.nq.gz
│   ├── 1d072195e6fce3ab8306605c83779cb902256383.nq.gz
│   ├── 2222b6e7f24afa2fd0eb2f7f3ed87593532984ee.nq.gz
│   ├── 39a1a05d0d4aa1f8df8be6c817316b271833c55f.nq.gz
│   ├── 5e3127b0fd5372d1c10c62a566aac6aa2ad9ed6b.nq.gz
│   ├── 67756caf9dd61554a7608635d1b02267c513905d.nq.gz
│   ├── 72b24f6707833f853ed64c9f7217d1e7096da216.nq.gz
│   ├── 72e8ffc0db8aad71a934dd11e5968bd5109e54b4.nq.gz
│   ├── 83fb45856e1daca34d3a15a1a2f9f1002eb80cd3.nq.gz
│   ├── 8dada3edaf50dbc082c9a125058f25def75e625a.nq.gz
│   ├── a82def68598fb003f3dd261170c62cf732a68dc1.nq.gz
│   ├── ae3cef240ec4adf8ba941df18e6b9dc036360d10.nq.gz
│   ├── af0bc7c588d7c6c265206e894053039f3c3b766c.nq.gz
│   ├── b14c0e50d5f25101d155abeb1ea3c27a0bac5a46.nq.gz
│   ├── b82ebc299739cf631507e5b53aa3f5751a9e2c82.nq.gz
│   ├── e5596c9fa000c4ebcd9acdbf8344e6f56f905713.nq.gz
│   ├── e8644a0264c7d9786c4138dac97e58f4dacf77c8.nq.gz
│   ├── f17b426251c12a291e6b531a5c01f451396d0dec.nq.gz
│   └── f55ee3d9cc8bf1496893c2fcefc03819883fb7d9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── aa82d02de61b7c9257853da4fc85f156c55d85ea.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 26 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[agronholm/cysystemd](https://github.com/agronholm/cysystemd)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
