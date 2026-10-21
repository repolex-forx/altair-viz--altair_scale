# Repolex Knowledge Graph of altair-viz/altair_scale

RDF knowledge graph data for [altair-viz/altair_scale](https://github.com/altair-viz/altair_scale), parsed by [repolex](https://repolex.ai).

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
rlex download altair-viz/altair_scale
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 46fda7e2fdf9d5f6bb043b976dd36af76552208e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 46fda7e2fdf9d5f6bb043b976dd36af76552208e
│           └── chunk-001.nq.gz
├── blob
│   ├── 25d09018126d2bde4d78abe74fa89263dcc0fbad.nq.gz
│   ├── 72364f99fe4bf8d5262df3b19b33102aeaa791e5.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── c6cc3475e32156bef1447e049e0bf4469c3fc5fb.nq.gz
│   └── ec09483dddb366ef33ed48d796cb1b6d259058ca.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 46fda7e2fdf9d5f6bb043b976dd36af76552208e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 11 files
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

[altair-viz/altair_scale](https://github.com/altair-viz/altair_scale)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
