# Repolex Knowledge Graph of asimov-modules/asimov-template-module

RDF knowledge graph data for [asimov-modules/asimov-template-module](https://github.com/asimov-modules/asimov-template-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-template-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e1efc722133adfef3a3224d66d6be3fe6a38c11f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── e1efc722133adfef3a3224d66d6be3fe6a38c11f.nq.gz
│   └── repolex
│       └── e1efc722133adfef3a3224d66d6be3fe6a38c11f
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 17887660b46a54e5eb6a74b3be3a8d3fbcd5310d.nq.gz
│   ├── 1d013ff92fa855fb03f148d15f9488c339392020.nq.gz
│   ├── 20c240c279ffafed6a0539670b6af566798893d1.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 4daabde3d2423750b7f7c12a9d0e60bd8fc7d051.nq.gz
│   ├── 561bded07990df561b61d488d4441b886322af9a.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 77d6f4ca23711533e724789a0a0045eab28c5ea6.nq.gz
│   ├── 79c79618be771f01008eaa2ad7076a2e499476ae.nq.gz
│   ├── 8758b2d80dbf8df05689fb8ad6fdeeb7225cb127.nq.gz
│   ├── 8b862e8576bee744ba8c5970c7dadb805c05e9d1.nq.gz
│   ├── 967edde49a597c4ccfd40a4d4237af5e2a948dcc.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c5e5bb9cfd39b6b948d2e16b1a33692f6f714d83.nq.gz
│   ├── c9479375f093e94bbe3b2803d17a8fbddc8a97cf.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── e1efc722133adfef3a3224d66d6be3fe6a38c11f.nq.gz
├── filetree
│   └── e1efc722133adfef3a3224d66d6be3fe6a38c11f.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 32 files
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

[asimov-modules/asimov-template-module](https://github.com/asimov-modules/asimov-template-module)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
