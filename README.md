# Repolex Knowledge Graph of scrapy-plugins/scrapy-jsonrpc

RDF knowledge graph data for [scrapy-plugins/scrapy-jsonrpc](https://github.com/scrapy-plugins/scrapy-jsonrpc), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy-plugins/scrapy-jsonrpc
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 15e0b7018c003ac794a1f9ce527397ca5602219a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 15e0b7018c003ac794a1f9ce527397ca5602219a
│           └── chunk-001.nq.gz
├── blob
│   ├── 1da73020d5a31d33331a88a07a1a989f16356ee0.nq.gz
│   ├── 20915c26be42224159d90a09d7edc3129a57d1d2.nq.gz
│   ├── 21b19e089a76f1eba7fcf18dce849c739f515c3d.nq.gz
│   ├── 41b1f4ed2427f1614c166c811bb8100ad8a1857c.nq.gz
│   ├── 4fff38c335067f852132f493a878d8ec5690bd34.nq.gz
│   ├── 55f42a23e0e005ea68b035c83e932213eecf7537.nq.gz
│   ├── 5c34e54f79f13761285ed28c6bb705267e7e0868.nq.gz
│   ├── 648404c7df6d3b0c09abb62e7abcc87348b64fcb.nq.gz
│   ├── 678d492f17912fc877f626df62894b3db3decd18.nq.gz
│   ├── 68067aac9cc65e7f65429565d7d552a3f585640d.nq.gz
│   ├── 6a9e53dcd2247510c4ca61dfa577d9d72a5369a6.nq.gz
│   ├── 6bf0890be9725ddd0af3f9cbb7ecb4f4084db362.nq.gz
│   ├── 7710bde8d7b673dc5ef14d25060a590f38cdbc0c.nq.gz
│   ├── c59182d164b0ba6884bc5137c3225137a9705097.nq.gz
│   ├── d505135b9b883982632f7e05e99f309c139fb654.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 15e0b7018c003ac794a1f9ce527397ca5602219a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[scrapy-plugins/scrapy-jsonrpc](https://github.com/scrapy-plugins/scrapy-jsonrpc)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
