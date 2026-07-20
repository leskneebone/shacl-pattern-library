# 0003 — Catalogue name and development namespace

Status: provisional
Date: 2026-07-20

Adopt **SHACL Pattern Catalogue**, abbreviated **SPC**, in place of the
project's previous working name. “Catalogue” describes the discovery layer
without implying that every catalogued pattern is directly importable. It also
aligns the project language with its DCAT-based catalogue model.

The source repository is named `shacl-pattern-catalogue`; the vocabulary uses
the `spc:` prefix; and development resources use the provisional base
`https://w3id.org/shacl-pattern-catalogue/dev/`. The ontology source file is
`ontology/spc.ttl`.

The former prefix and development base were unreleased identifiers with no
registered redirect or persistence commitment. This refactor therefore
replaces them rather than asserting semantic equivalence. No old IRI is to be
recycled for another resource.

The Australian spelling **catalogue** is canonical in project names and
identifiers. **Catalog** may be supplied as an English-language search label,
but it does not identify a separate project or vocabulary.
