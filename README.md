# Repolex Knowledge Graph of bentoml/Pneumonia-Detection-Demo

RDF knowledge graph data for [bentoml/Pneumonia-Detection-Demo](https://github.com/bentoml/Pneumonia-Detection-Demo), parsed by [repolex](https://repolex.ai).

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
rlex download bentoml/Pneumonia-Detection-Demo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6e5efd649558ea6e85ce1fdf8e552d5dc89cc973
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6e5efd649558ea6e85ce1fdf8e552d5dc89cc973
│           └── chunk-001.nq.gz
├── blob
│   ├── 02c03953e4dfca81c79c3ca4af59a79c28df8a63.nq.gz
│   ├── 09d4fcad27e1c634ee862a7fe53410d1a177bad7.nq.gz
│   ├── 10ade34c12f77722383e412e8e5972e395b8f25e.nq.gz
│   ├── 25fdf4b35aa318d0dd27f6bef761b570a1edc10a.nq.gz
│   ├── 278a099e6eff160f6da27dfa2a99fc5d92de4692.nq.gz
│   ├── 2dd56ff32bb838de4a94e220af8b6c65a69ac35b.nq.gz
│   ├── 336f28fddde09195302815d53bbcf2c3b073955d.nq.gz
│   ├── 57259504b70a8e335fedb391cf84c27b2e7aadc3.nq.gz
│   ├── 9388c583fe342e8a60a291ba1aaafc53b883900a.nq.gz
│   ├── 99d798ea91bd261e6773f94b62487e47cdc2a19e.nq.gz
│   ├── a6aed0b68fc6ef72003d1a1ae54b22f6e3ee694c.nq.gz
│   ├── a8a8ad60c823cf1a09cb69c79027048eb77d909a.nq.gz
│   ├── aba8d7fc29c18624ccb7fc2b24840543bba08c8a.nq.gz
│   ├── b30da70698433c565f71ad5f7dca5156dac8da0a.nq.gz
│   ├── b3df526e059a2bdb1459b0183118659683c7b267.nq.gz
│   ├── c4f7baf3ebea9acae51d0dab853e9c154274c113.nq.gz
│   ├── ce852263419115c3980f7aab97fddae33a3fdc91.nq.gz
│   ├── cfb813a2011e0f177590f7ae9bfbd970428b074b.nq.gz
│   ├── d08d0d0f996cb26ccb126fb30ad1699ed5a26b6c.nq.gz
│   ├── e566bcb28d688b14213f8f912a279f017e35b37f.nq.gz
│   ├── eb47b123e22b24bce9e2bac53402337a0e76c857.nq.gz
│   ├── ee251efeea851eb0d8af8a3a3073147188d52f09.nq.gz
│   └── f56088b735860c84714c22a8d608b310e1e22a57.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6e5efd649558ea6e85ce1fdf8e552d5dc89cc973.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[bentoml/Pneumonia-Detection-Demo](https://github.com/bentoml/Pneumonia-Detection-Demo)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
