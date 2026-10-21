# Repolex Knowledge Graph of jupyterhub/jupyterhub-deploy-hpc

RDF knowledge graph data for [jupyterhub/jupyterhub-deploy-hpc](https://github.com/jupyterhub/jupyterhub-deploy-hpc), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/jupyterhub-deploy-hpc
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fbffef1aacf15f656ca6a1b7b2b24906212263d7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fbffef1aacf15f656ca6a1b7b2b24906212263d7
│           └── chunk-001.nq.gz
├── blob
│   ├── 03cc728b204ef50d2cd4fe1cd4cd2c27f84f3d18.nq.gz
│   ├── 17e783f02d559cbc6d436a381d6f5a18ceed99ba.nq.gz
│   ├── 5520ebb429c7601122fadc23f4f2c50bfea9b69d.nq.gz
│   ├── 5a6a65062440bead82b6fd8892fc65b5e8544361.nq.gz
│   ├── 5e6986c9de2a04c4986d5deaec2d98f9fbabd54d.nq.gz
│   ├── 5faeb7b69015bba9fc12685642ffe79d396bc50d.nq.gz
│   ├── 61d470004218ae459ce7bfdc974f7c86e0790486.nq.gz
│   ├── 659f6407694650c9b60a536b24f5be42f56c360d.nq.gz
│   ├── 6f0345bcc5c9d11126c9cafc32d2749fa97fd332.nq.gz
│   ├── 815a9af14e2dd40f998a82afe49089c84b973810.nq.gz
│   ├── 87b0fccfd933d2ddb63b55e3346645872a27ae4c.nq.gz
│   ├── a2bad5eb7c74e88f64de347464c2dbed5648592f.nq.gz
│   ├── a46bda272bc83f6fe06d804f448ad1fc56176ff5.nq.gz
│   ├── d9b1476bb2610c2411ccebd8449996f254b4cdb5.nq.gz
│   ├── ec4b9303df98ed9a46ee93ad476d0d863ca95ce1.nq.gz
│   └── fc8da63c3223e8e19ddc81f1908c22b7bc40f025.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fbffef1aacf15f656ca6a1b7b2b24906212263d7.nq.gz
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

[jupyterhub/jupyterhub-deploy-hpc](https://github.com/jupyterhub/jupyterhub-deploy-hpc)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
