# Repolex Knowledge Graph of pytest-dev/pytest-splinter

RDF knowledge graph data for [pytest-dev/pytest-splinter](https://github.com/pytest-dev/pytest-splinter), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-splinter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1b0aa1efaec40919d79d424bb6d5c418925f2ad6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1b0aa1efaec40919d79d424bb6d5c418925f2ad6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b9f9ab5ee01d506f1dc3d1f70e0a435d61d368f.nq.gz
│   ├── 0c2444c46f1247fbfca89cff6d70621638b98ddb.nq.gz
│   ├── 1b5d66269d98e9a8a47ec9d3af0820f5db600317.nq.gz
│   ├── 22f676d040ebe8fcc7f1a4ce82126484df865205.nq.gz
│   ├── 27046296f73b21558efe546e48804a79c617777d.nq.gz
│   ├── 33d57c89fca834a67830f6052c79a14d4dec6e39.nq.gz
│   ├── 40ed8d3f2feac396e5533898e0c86271dbf5b29a.nq.gz
│   ├── 5a076b68b724705ad7f4f786872bd044cb466451.nq.gz
│   ├── 684788eacc1859addcf0fd965c703458a17158d0.nq.gz
│   ├── 6ab6e89406f249465495d05fa01f5c1d4d71cb98.nq.gz
│   ├── 6c6ffd63dd530cd5f4c3414a2a5011f08069f933.nq.gz
│   ├── 6e646b306192ff50b03b9c32a92c4284e55cfc5c.nq.gz
│   ├── 74fc1f1d7b3889c9a98f89b3e0e1e0c295dcb955.nq.gz
│   ├── 7ff62265cfa12c21f44360c20d540f01bb9b06bb.nq.gz
│   ├── 806f98a5e3fe851c1fead4c41a6e52f30f0b2b4d.nq.gz
│   ├── 88fd00301b9b757c2dd2dbc9edfad2893c15947d.nq.gz
│   ├── 8a5f63152e87cd814580bf50ce43c3219a0f41cd.nq.gz
│   ├── 92266013326f8825d2a36f08ba8fe45362724455.nq.gz
│   ├── 97d0c9fde05eaac44271a536ba707e7c91ef89d5.nq.gz
│   ├── ae46bd9dd9efb26e904cb9e689c09a7b0c3dce4d.nq.gz
│   ├── b1b96290c7c34405f27a857b4e810e044984a89c.nq.gz
│   ├── be8679b7a7af82839c18c6f09164bda8b49d6f98.nq.gz
│   ├── bfe74b1c709b44c5fbef9b8b6da18d4cdb58b4c0.nq.gz
│   ├── c3f263973181e259a9ad8b19acea81f868b55d6a.nq.gz
│   ├── c5e12310bf5d5aebc873a998a498ae34988ada18.nq.gz
│   ├── c6d3a3b1d7273bdf299bd93516988ef16eb748c3.nq.gz
│   ├── c712d2595247bf32129c8609dcf822e238412a20.nq.gz
│   ├── ca62ad6f4d2b2422d27d98d243736fc11bfa7e2f.nq.gz
│   ├── cb5f862afad76f1b275db8fd13bd64f28d95e5f7.nq.gz
│   ├── d529f969ade957b7a7b4e664cf4487b2a728fe00.nq.gz
│   ├── e393af3a00475f2fc3da4fb4e499e8d9139c353b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f20f3b61c727d24d9de6e22fdb95cbec32fc319c.nq.gz
│   └── f8641716f80e4bb57d28b56e823ebd8d85ddc6fe.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1b0aa1efaec40919d79d424bb6d5c418925f2ad6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[pytest-dev/pytest-splinter](https://github.com/pytest-dev/pytest-splinter)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
