# Repolex Knowledge Graph of rust-native-tls/rust-native-tls

RDF knowledge graph data for [rust-native-tls/rust-native-tls](https://github.com/rust-native-tls/rust-native-tls), parsed by [repolex](https://repolex.ai).

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
rlex download rust-native-tls/rust-native-tls
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3cf1877ee86814168255db6d73fbefc127211c1c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3cf1877ee86814168255db6d73fbefc127211c1c.nq.gz
│   └── repolex
│       └── 3cf1877ee86814168255db6d73fbefc127211c1c
│           └── chunk-001.nq.gz
├── blob
│   ├── 1332f8eb5d96f1551077bd11558a8805cbb8f9f1.nq.gz
│   ├── 1a97adc0f4430344b3e934104d46745451bd7041.nq.gz
│   ├── 23d7b1ad10542af695a5571b3a3dbe51c96147fd.nq.gz
│   ├── 2deeb18eccc3d1bb44c0079875e59dd6430e3405.nq.gz
│   ├── 483be948cc57ebadf04b92e702ad0d3845be28c8.nq.gz
│   ├── 4e3ddddc3005a0fd621794bb7061e8b3f8a9a1e1.nq.gz
│   ├── 58672e2642c6de7f904c8a544b2657f2963921a6.nq.gz
│   ├── 74f08c6647857d9bb1ce2c08cfbc722841e0986c.nq.gz
│   ├── 8595008d3a8acb500fb3ba3a0a1d01b739183153.nq.gz
│   ├── 8f71f43fee3f78649d238238cbde51e6d7055c82.nq.gz
│   ├── 981a42dc9d761c6deda8e0cd671109497aeeb268.nq.gz
│   ├── a112c29826a486375a97b849863f519e2fb37acc.nq.gz
│   ├── abc6f14c43101006e1749bbb90b97549ba58e2ac.nq.gz
│   ├── b2bbae1c78e75dbc428813a0e7f2a45b7d9471e1.nq.gz
│   ├── bc3d32255aa038a570482e1d70979d888ff00f47.nq.gz
│   ├── bcf45424530da5080e8d7db449ac53d895b0cdae.nq.gz
│   └── dc1c9209572708387e9803ca4fe8c325129f1006.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3cf1877ee86814168255db6d73fbefc127211c1c.nq.gz
├── filetree
│   └── 3cf1877ee86814168255db6d73fbefc127211c1c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

[rust-native-tls/rust-native-tls](https://github.com/rust-native-tls/rust-native-tls)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
