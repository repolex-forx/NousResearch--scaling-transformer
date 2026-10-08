# Repolex Knowledge Graph of NousResearch/scaling-transformer

RDF knowledge graph data for [NousResearch/scaling-transformer](https://github.com/NousResearch/scaling-transformer), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/scaling-transformer
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 478cdd2a2a78038c99adbf161c2de2b9fc5993ef
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 478cdd2a2a78038c99adbf161c2de2b9fc5993ef.nq.gz
│   └── repolex
│       └── 478cdd2a2a78038c99adbf161c2de2b9fc5993ef
│           └── chunk-001.nq.gz
├── blob
│   ├── 141a67045945005d88540e9e395d33d41a364079.nq.gz
│   ├── 18143f37b9be63ee2dcaac39c1d2cbafac1c8ea9.nq.gz
│   ├── 25905e72e4298dac880d922987cc23eba3441b21.nq.gz
│   ├── 2f980f363b7732995f7386a6f088d4f8b142718c.nq.gz
│   ├── 47b71350a515b43776dec843d3cbdae3e0031b03.nq.gz
│   ├── 65efb979ffb3ea06475d4688fa656ed61c153a9d.nq.gz
│   ├── 6855e4dcd568f4c22867b58110cd2092044a6ff6.nq.gz
│   ├── 69fc416a1696d44ed359c76647e798d06fcc8817.nq.gz
│   ├── 6bd9e3eec444ca6116f74b1fcd6c471099abcb36.nq.gz
│   ├── 6f9567541892cb433baad0121b443c0571f3795e.nq.gz
│   ├── 7940ac10385c8c8a7b8f4943bcc1e956479b5460.nq.gz
│   ├── 7b21878e24a3ec9bfc56fd04769780472d2454e5.nq.gz
│   ├── 8519a2e3a9e4ba94fe7169455272206eea8350ed.nq.gz
│   ├── 90e401fe50cfb8aa150e1ba802ed87282aef9589.nq.gz
│   ├── ad3dc66984b69d6bb21793776e38749416dc782c.nq.gz
│   ├── b61cd516f6bb0ad2ddc2146295d6f7498f65952d.nq.gz
│   ├── b657ccfa7dafa7027e67eafedfc32d975cab9f88.nq.gz
│   ├── c7f28d09b021611178fe4d038ef24b9d77c49ef3.nq.gz
│   ├── ce7dd9f23549d2e958b401d19ec058cd3e82bcca.nq.gz
│   ├── d759018e5e515a5ce5cbae4fd5ac127f0830cc1e.nq.gz
│   ├── e1ce3f4248d93065c3037b703bbfac2c71088bad.nq.gz
│   └── f4c53a759cea6ecf1cc1bb2672748ea758b159c3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 478cdd2a2a78038c99adbf161c2de2b9fc5993ef.nq.gz
├── filetree
│   └── 478cdd2a2a78038c99adbf161c2de2b9fc5993ef.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[NousResearch/scaling-transformer](https://github.com/NousResearch/scaling-transformer)

---
*Parsed on 2026-10-08 by [repolex](https://repolex.ai)*
