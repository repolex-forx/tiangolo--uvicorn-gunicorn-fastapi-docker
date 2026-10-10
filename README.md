# Repolex Knowledge Graph of tiangolo/uvicorn-gunicorn-fastapi-docker

RDF knowledge graph data for [tiangolo/uvicorn-gunicorn-fastapi-docker](https://github.com/tiangolo/uvicorn-gunicorn-fastapi-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/uvicorn-gunicorn-fastapi-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c93bb25d29df09a5a19ebaa4ea533aa6c63b637e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c93bb25d29df09a5a19ebaa4ea533aa6c63b637e
│           └── chunk-001.nq.gz
├── blob
│   ├── 1ae5021d1785b5e649364ca061e7bd19dcc0edde.nq.gz
│   ├── 236a646ecff2caf37d6743a6dbb5324583ba0dc8.nq.gz
│   ├── 2811ded3331f0482bdee78628f167c7668741729.nq.gz
│   ├── 2ca579c6fe5234a52fbc2aa9ee7eb2a6ac93714f.nq.gz
│   ├── 30f6eb1d40a89985cd77e10b82bc165a3377bcf3.nq.gz
│   ├── 42f45187b73abf358695d47408b6ea2156828e22.nq.gz
│   ├── 53dd60afa903ec0b511cc9ec7cc14c19308fad84.nq.gz
│   ├── 55eec6eb458d17b0a36c90625488d8fafbda90d5.nq.gz
│   ├── 5fc5f542be61a8ec27f104a4685be273a6350ebd.nq.gz
│   ├── 60c586173fca860d106e8c2be40cbb68be5a544f.nq.gz
│   ├── 6b9e6f99bb5f6047a0b3e32fa40450cf88bfcd29.nq.gz
│   ├── 7640fd5f71d83ee12db0977b8db4cfc1d55bae6d.nq.gz
│   ├── b949877eb4748a0d1f44d801f8ace7bab534487e.nq.gz
│   ├── dc386f81a91d5f8cdd69dc4e6e8d8c85f361ada0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec967e98a4831519d3747165d04d2d96cd7ec51b.nq.gz
│   ├── f4db468478974cd73fbe3c9fee8a545d7aaf3f68.nq.gz
│   ├── fbc78f2caa865a690f48ee48cc34a849166f645c.nq.gz
│   └── feec529f1e6a2c68172ce4c39dca6419764cdbfa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c93bb25d29df09a5a19ebaa4ea533aa6c63b637e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[tiangolo/uvicorn-gunicorn-fastapi-docker](https://github.com/tiangolo/uvicorn-gunicorn-fastapi-docker)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
