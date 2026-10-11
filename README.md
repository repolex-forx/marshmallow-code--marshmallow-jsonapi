# Repolex Knowledge Graph of marshmallow-code/marshmallow-jsonapi

RDF knowledge graph data for [marshmallow-code/marshmallow-jsonapi](https://github.com/marshmallow-code/marshmallow-jsonapi), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/marshmallow-jsonapi
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e7273b4c3e6b7bad6279302caef2a87c96fbb785
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e7273b4c3e6b7bad6279302caef2a87c96fbb785
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e16527fd37c93fe2727ef0562542fbcf0a2745b.nq.gz
│   ├── 0e35bee91470117571d29550419477dba7f42c93.nq.gz
│   ├── 159d78015a70fd72bd07f06068a7498b25e3d5a4.nq.gz
│   ├── 1ce272c23ea30f548f0b81fe99ed95ddcc85568d.nq.gz
│   ├── 2df9a8cbbb680a1e83d41f835efafaefffc4888b.nq.gz
│   ├── 2e10ac499186d2cf5a52d798773e7f66ef854ec0.nq.gz
│   ├── 3203b2ca1eb88effedf7bea1bac03648c108e092.nq.gz
│   ├── 411fea496f8560a5fe1ececf487bf487884071ec.nq.gz
│   ├── 4e1ef159d7f2237a6e408d4858a675d443deebb4.nq.gz
│   ├── 51202cee5d294de5ef673c8e2a6e0c12f1668644.nq.gz
│   ├── 6363236b68a589b8255082665e3905c867e122c6.nq.gz
│   ├── 63ca2e3d5fc93dd525e8eea6b570463de45a7297.nq.gz
│   ├── 6958d673885f8164af756506f60243f5b6070da1.nq.gz
│   ├── 76888fe1bf10912f9575845efabb510921743065.nq.gz
│   ├── 80d76af5f28ddd3b1e2a248548bb19883afe5337.nq.gz
│   ├── 95aebfa5c1e742f9b98c1a34928ef5133cc6b396.nq.gz
│   ├── 95e719e5a6a68b7c768ecb2ebc9796d8c81cc1c7.nq.gz
│   ├── a91ba9e0fb8243e8d0caad788a392756dfbe5d73.nq.gz
│   ├── aa8b247fb2b49213cc0715932c4ad234ed02ca54.nq.gz
│   ├── af7cf8dcc25c1fde41a0cd6c280b867bace90f6f.nq.gz
│   ├── afb095ecd965738d7215e242da0b3668385a3f7e.nq.gz
│   ├── b2d7bc3107d184fa0b75d180cdb7da15a6630af0.nq.gz
│   ├── b32babbe003bd6119d8b7bc6cf7df6cd86d52df9.nq.gz
│   ├── b6a34dbfe37f676f2c093476f0b1a08c0d1de345.nq.gz
│   ├── be677f5d3b77effc7cb89236672090e2bc628df3.nq.gz
│   ├── bf8cea37254c2580c0bacdfcf60d7212996dc5a3.nq.gz
│   ├── c2495148f81051fd3adfe4e1b4f8969a7a38d2c6.nq.gz
│   ├── d1ca7e703a9871d42e690d81b54867cd21afe0e6.nq.gz
│   ├── d2ea971c78968cb6038877e9366d82c4d3fb0f0f.nq.gz
│   ├── d98e7dccd813bd5c0f9a28dc8e0a46011e7cdef1.nq.gz
│   ├── e122f914a87b277e565fc9567af1a7545ec9872b.nq.gz
│   ├── e3ad939ae2d1775a8543c8a77a2bd2b38794975d.nq.gz
│   ├── e582053ea018c369be05aae96cf730744f1dc616.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee9c2cf7c471de6559d982ba474cf19af1357aa2.nq.gz
│   ├── f15def3bb873c29776fc3dbf97ebb851fe85ecc7.nq.gz
│   ├── f56174a9e3ee820b02be28a217d0b4e35b435371.nq.gz
│   ├── f715c92808e71a6c6fb220fc42aa9492cd716d9f.nq.gz
│   └── fa07e9e9a0a642238290e1e531c015e7134401fa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e7273b4c3e6b7bad6279302caef2a87c96fbb785.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[marshmallow-code/marshmallow-jsonapi](https://github.com/marshmallow-code/marshmallow-jsonapi)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
