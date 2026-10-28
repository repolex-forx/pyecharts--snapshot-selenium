# Repolex Knowledge Graph of pyecharts/snapshot-selenium

RDF knowledge graph data for [pyecharts/snapshot-selenium](https://github.com/pyecharts/snapshot-selenium), parsed by [repolex](https://repolex.ai).

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
rlex download pyecharts/snapshot-selenium
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 19b281ce89062eac35767ce7e97be570dbde3635
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 19b281ce89062eac35767ce7e97be570dbde3635
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c2d32faa40353cd52a7af35837bc51e8b53d791.nq.gz
│   ├── 1095366a5e4150086b805ac195c438675425c315.nq.gz
│   ├── 14247d23eddcc542a65e10203b3bfe44d30b9c2d.nq.gz
│   ├── 293a48fa2a616b101c2afd58ab8b83a126a3f3a0.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 38635bb7845762a7c702be940a63cea31f2d8504.nq.gz
│   ├── 3e0522964fb56a69364871c0881e14e0d5f8104d.nq.gz
│   ├── 3e0ee51423673045d76cf8604c03cc0c6432c58a.nq.gz
│   ├── 5f13ef040f26a35f377fb13a2a48b1a07f973ba0.nq.gz
│   ├── 6d52a60951bb0459cdbe7919de642c11d02eca87.nq.gz
│   ├── 6fdff773040f3a0492edac66645bc5b75d015bd1.nq.gz
│   ├── 7cb6656b279f2ababe7e6c20313404c71202e2d4.nq.gz
│   ├── 9d7ac2db175f83f347d37ca5a08ca60e67ac4c9f.nq.gz
│   ├── 9dcc3299ef03e7c2f6ce3f61e460dc01a5599027.nq.gz
│   ├── a17955cf62e2a0322251933ca7695ed3f088025b.nq.gz
│   ├── b70c2782aa78ff135cc4dadbe992727e9a67596b.nq.gz
│   ├── c0bd2f4a9abd1f9e0e0e436dd76167c08eb64d0e.nq.gz
│   ├── d31eeaa644fa18b29af15f226cc02daa5ad59227.nq.gz
│   ├── e7f35d6df6cb660163fa742d45c8eca8c045b225.nq.gz
│   └── f926159474b3f333d62247066377271f55590fc0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 19b281ce89062eac35767ce7e97be570dbde3635.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[pyecharts/snapshot-selenium](https://github.com/pyecharts/snapshot-selenium)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
