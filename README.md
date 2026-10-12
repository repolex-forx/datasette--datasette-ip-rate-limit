# Repolex Knowledge Graph of datasette/datasette-ip-rate-limit

RDF knowledge graph data for [datasette/datasette-ip-rate-limit](https://github.com/datasette/datasette-ip-rate-limit), parsed by [repolex](https://repolex.ai).

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
rlex download datasette/datasette-ip-rate-limit
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8d338b0898d7e7e816f90723e99e219993c307c5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8d338b0898d7e7e816f90723e99e219993c307c5
│           └── chunk-001.nq.gz
├── blob
│   ├── 2389cb66428a39c9c0bf14033ce7cba25a5e998e.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2cb3830868588c1f13976492eb6bd52cd17bbbe4.nq.gz
│   ├── 3eb871944ba060e652582342cecb018b41f78bda.nq.gz
│   ├── 5c9664cc4c7beafe76feba5db06b5ed6b88a78d6.nq.gz
│   ├── d49d309499efb2c0c1d38efdd53056249a7d74d8.nq.gz
│   ├── e7931a368881c7aed1880a2eb4a186215198573b.nq.gz
│   └── eb22e74eaaaf0edc4aa2c0f8900a55750d1660f9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8d338b0898d7e7e816f90723e99e219993c307c5.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 14 files
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

[datasette/datasette-ip-rate-limit](https://github.com/datasette/datasette-ip-rate-limit)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
