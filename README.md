# Repolex Knowledge Graph of jaraco/jaraco.home

RDF knowledge graph data for [jaraco/jaraco.home](https://github.com/jaraco/jaraco.home), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.home
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 394e968592bb93f5c1b2f8112fa414e733ec6bc3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 394e968592bb93f5c1b2f8112fa414e733ec6bc3
│           └── chunk-001.nq.gz
├── blob
│   ├── 10d5851fd2f23de76e9bd688c93056774fd14e7c.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 30779d158b0656d72c8bb738b6e1d33a3a391da1.nq.gz
│   ├── 3095274d3c0b6d900153c9ebd9930961aea99ee0.nq.gz
│   ├── 432ebec63acb862e0b230ce68c5fd97bc2178ebd.nq.gz
│   ├── 52b72d3d1c7105b0669afe61479afd51d1105086.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 5c718fb5b0c4099eafd7d267313be26a88d4dbf7.nq.gz
│   ├── 65fe51a2bbeb34f9c1923d8bde884ceb9071f9e9.nq.gz
│   ├── 6eab7c7c2767ef8089decc1bcd5c9b7e49432600.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 8520aa170f0d61d26ef3ad25e39ae898543017d2.nq.gz
│   ├── 8dae942974157d9388ca766c41ece10be1c0e31f.nq.gz
│   ├── 9da945bc79e542031c645f7caa801f4b2426812e.nq.gz
│   ├── 9f810aaa5b954c47845f4a781d664ce466a38511.nq.gz
│   ├── a18d5f4391c12238951dcd791f05105cec0c5437.nq.gz
│   ├── b34cc687bff25e505d298b0fcd6e4f7747b3afb1.nq.gz
│   ├── c20f10e8bc8edbd6cd14b32f717030f2afb75229.nq.gz
│   ├── dc5f6a537cf06976f8297609233c4d88a73b7544.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ede7c5bdd6fe66ba643f63e726eee3cd2023fd98.nq.gz
│   └── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 394e968592bb93f5c1b2f8112fa414e733ec6bc3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[jaraco/jaraco.home](https://github.com/jaraco/jaraco.home)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
