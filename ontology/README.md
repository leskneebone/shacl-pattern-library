# Catalogue vocabulary

[`spl.ttl`](spl.ttl) is the first development draft of the SHACL Pattern
Library vocabulary. It defines only local classes that the architecture needs.
It deliberately defines no local properties yet.

Relationships in the first manifests reuse DCAT 3, DCTERMS, ADMS, PROV-O,
SHACL and OWL terms. When an existing property is too broad or carries the
wrong semantics, the mismatch must be recorded before a local property is
proposed. Candidate terms must also be checked against established vocabulary
registries and source vocabularies; matching labels alone are not evidence of
matching semantics.

The draft namespace is provisional and carries no persistence commitment. The
ontology is an experiment, not a released vocabulary.

## Initial distinctions

- A `spl:ValidationPattern` is the conceptual catalogue item.
- A `spl:PatternVersion` is an immutable version of that item.
- A `spl:PatternModule` packages reusable SHACL material.
- An `spl:ExecutableModule` is a module that is executable without unresolved
  bindings; it is also a `dcat:Dataset`.
- A `spl:PatternTemplate` still requires declared bindings or specialisation.
- `spl:PatternRole`, `spl:Parameter`, `spl:Mapping`, and `spl:Assembly` name
  supporting architectural resources without yet prescribing their relations.

The Schema.org projection is not asserted in this ontology. In particular,
`schema:pattern` is not used: it describes surface or print designs, not
validation designs.

## Validation

Validate the OntPub MUST requirements with [Kurra](https://github.com/Kurrawong/kurra) locally cached Ontology
Publication Profile validator (currently validator ID 20):

```shell
kurra shacl validate ontology/spl.ttl -s 20 --hide-warnings
```

Kurra renders validation results with Rich before a pager receives them.
Consequently, `less -S` alone cannot recover IRIs that Rich has already
truncated to the detected terminal width. When sending the output through a
pipe, set a wider virtual terminal first:

```shell
COLUMNS=320 kurra shacl validate ontology/spl.ttl -s 20 | less -S
```

Increase `COLUMNS` further for unusually long focus-node IRIs or messages. A
future Kurra output option such as CSV, Turtle, or an explicit table-width flag
would be preferable when lossless machine-readable results are required.
