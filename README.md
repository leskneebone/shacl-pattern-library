# SHACL Pattern Catalogue

An exploratory, personally maintained project investigating whether common SHACL validation designs can be made safer to reuse than copied shapes.

The name describes a **catalogue of patterns**: documented validation designs that may include executable modules, parameters, mappings, examples, and tests. A pattern is not necessarily a shapes graph that consumers should import unchanged.

## Status

This repository is pre-alpha and architectural. Nothing here is a standard, a universal best practice, or production-ready. Its ownership, governance, canonical namespace, and publication authority are deliberately undecided.

The current development namespace is `https://w3id.org/shacl-pattern-catalogue/dev/` as a conspicuous placeholder only. It is not registered, promised, or suitable for external dependency. See [IRI and namespace requirements](docs/iri-and-namespace-requirements.md).

Examples abbreviate that namespace as `spc:`. The repository name, vocabulary file, and development IRIs use the Australian spelling “catalogue”; “catalog” is an English-language search label only.

## Intended users and scenarios

- shape authors adapting a proven constraint design to a local data model;
- profile maintainers assembling tested patterns into an application shapes graph;
- tool builders generating specialised shapes from abstract roles and mappings;
- reviewers comparing portability, performance, and semantic trade-offs;
- publishers exposing pattern metadata through ValPub-compatible profiles.

The primary reuse scenarios are selection and adaptation, deterministic assembly, and—only where explicitly declared safe—direct module import.

## Start here

- [Project charter](charter/CHARTER.md)
- [Concept assessment and risks](docs/concept-assessment.md)
- [Architecture](docs/architecture.md)
- [Pattern contract](docs/pattern-contract.md)
- [Testing and portability](docs/testing-and-portability.md)
- [Experimental patterns](patterns/README.md)
- [Open questions](docs/open-questions.md)

## Repository layout

The repository separates catalogue vocabulary (`ontology/`), opt-in external vocabulary alignments (`alignments/`), pattern packages (`patterns/`), abstract-to-local mappings (`mappings/`), assembly tooling (`tooling/`), publication profiles (`profiles/`), cross-pattern examples (`examples/`), and repository-level tests (`tests/`). This layout is provisional and follows the architecture rather than defining it.

## Licence and responsibility

The work is offered under [CC0 1.0](LICENSE) for maximally permissive reuse, subject to the separate [disclaimer](DISCLAIMER.md). Licence choice remains an architectural experiment and should be reviewed before a stable release.
