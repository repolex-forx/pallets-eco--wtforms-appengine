# Repolex Knowledge Graph of pallets-eco/wtforms-appengine

RDF knowledge graph data for [pallets-eco/wtforms-appengine](https://github.com/pallets-eco/wtforms-appengine), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/wtforms-appengine
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 230da3db8170b526322ee9b520ba23bd9e90ddac
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 230da3db8170b526322ee9b520ba23bd9e90ddac
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b338f70e64ccdcc2c031faf77348cc2eb19522e.nq.gz
│   ├── 0c6b801dc678eec21beb9830c3bcebdd28f9d596.nq.gz
│   ├── 19b243360c85e75dca09559d4d465ddf2de12a13.nq.gz
│   ├── 2602a29fe4af8838bdd84047b9e1b5c8da1cb4c7.nq.gz
│   ├── 3691b712b46ec1f5d01ee582f67f30fc2957d3cc.nq.gz
│   ├── 3b6a16dc97ee8b7ada398a5835418d061aa6d50d.nq.gz
│   ├── 532b1b587cf724c2c1985fee90294f0653302771.nq.gz
│   ├── 5867bbd9aa6ad3b752f8158ece0a6615bd30d176.nq.gz
│   ├── 5b852f82496e374d6f726c7f1f32bc4bdebde0ac.nq.gz
│   ├── 5fa1225ad7bafc74ac032aae9cdf42eeef8dda49.nq.gz
│   ├── 652eed5ffc9401731e4e089b31035c13f1269aa5.nq.gz
│   ├── 6f6abc5eaec5ecb6dc7475d61cefd4e9f007854e.nq.gz
│   ├── 738534c83caa118cc9d9a93758bb22e2167aa3fd.nq.gz
│   ├── 7b22498b19280fe1b67f4c210d68c7255c29bdd6.nq.gz
│   ├── 7c964b49e2db4d6983a3d8d56509162de9110035.nq.gz
│   ├── 8d1daa33b741e5d01afa391a5d2de52af3ff07de.nq.gz
│   ├── 9b0851f36c6346135169f85e279f739f5b3ffa1c.nq.gz
│   ├── a0bfa03a04b61f2503212b039814999021f6baa2.nq.gz
│   ├── a207fe47aa41f41729600ad0eaca85b39c9a7d9a.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── b93bc2c134d2aed498a525aad898a61556729d05.nq.gz
│   ├── ba8b9286d097e3ea0992276e8bd20e67609a2342.nq.gz
│   ├── d65b240a7b038437ccf2ef630f62c30e90a7a7dc.nq.gz
│   ├── daf72c266ec7d7f937cac2db461fd06f58c306d5.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ed2ab0f680e34c586cc5cc272b9512d28e284804.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 230da3db8170b526322ee9b520ba23bd9e90ddac.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[pallets-eco/wtforms-appengine](https://github.com/pallets-eco/wtforms-appengine)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
