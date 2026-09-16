# Repolex Knowledge Graph of florimondmanca/httpx-sse

RDF knowledge graph data for [florimondmanca/httpx-sse](https://github.com/florimondmanca/httpx-sse), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download florimondmanca/httpx-sse
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e8fcd9e159066185963ffb9fa29efb8ba2ca84bf
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── e8fcd9e159066185963ffb9fa29efb8ba2ca84bf.nq.gz
│   └── repolex
│       └── e8fcd9e159066185963ffb9fa29efb8ba2ca84bf
│           └── chunk-001.nq.gz
├── blob
│   ├── 017ed5eb3c0c09e64f74aa0fb985cdb6b1d3bd6f.nq.gz
│   ├── 08e627f6284d8b9b595365f7e28ab7dd4d2175bc.nq.gz
│   ├── 09e0c43d12f5e7f3e6038b1f43d467a094d70250.nq.gz
│   ├── 0f55825e303be27a5f53477dbc6fde1f747cbbea.nq.gz
│   ├── 1f6ad81f9eba8c0bd80908609a2f74b4b1097101.nq.gz
│   ├── 287e3844b0670f0eb967c39146848601181b3cf5.nq.gz
│   ├── 2dfcd1e393d922712f4d60501288c828eb78c4c4.nq.gz
│   ├── 30b0e7cbb2e3f61f7061695c9bc4d6087b94ca38.nq.gz
│   ├── 35bbeaff3a204bd40ecccec32da76c09de8cb3c2.nq.gz
│   ├── 36600eb63374cb1f936f4d90a9aa1ad5b5c1fd9f.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 49139e012b8905b8b421e488415d4e509f1838bc.nq.gz
│   ├── 5580482f3fefe5620609489b3e1682dddde5cdbc.nq.gz
│   ├── 5fe04c9962dd778b4d002fdb3ddbdb521e0f25e2.nq.gz
│   ├── 625638ab85e3289a33a254b2cfd69562011ecaee.nq.gz
│   ├── b83cf09a2d8e8d26e91bc3f74e92b1c7d7eaa7ca.nq.gz
│   ├── ba0b39ddcd10fa8812e528e4137dcb7e1b1a6e5d.nq.gz
│   ├── cd2c4d287ce86c4e922d56c66423615085892e14.nq.gz
│   ├── d0674c7cfb26768be6be423c0fd73edd07ae88c8.nq.gz
│   ├── d33434efde7a335e353e1e05e08cc5714e2524b4.nq.gz
│   ├── d4dc1190f7b02a8c97ab85e4f896787ca39dd9ec.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ef61825739cd0a4daf2303fd60010e99155208e4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── e8fcd9e159066185963ffb9fa29efb8ba2ca84bf.nq.gz
├── filetree
│   └── e8fcd9e159066185963ffb9fa29efb8ba2ca84bf.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 33 files
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

## Source repository

[florimondmanca/httpx-sse](https://github.com/florimondmanca/httpx-sse)

---
*Parsed on 2026-09-16 by [repolex](https://repolex.ai)*
