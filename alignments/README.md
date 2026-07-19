# External vocabulary alignments

This directory is open to alignments with any relevant external ontology or
vocabulary. Each external vocabulary receives a separate graph so its target
version, provenance, confidence, compatibility, and maintenance status can be
reviewed independently.

Alignment graphs are optional and are not imported by the core SPL ontology.
Consumers choose which graphs and entailments to accept. An alignment must cite
the dated version of an evolving source specification wherever possible.

Class-level `rdfs:subClassOf`, `owl:equivalentClass`, property-level
`rdfs:subPropertyOf`, and `owl:equivalentProperty` statements are used only when
their universal entailments are intended. When just one resource satisfies two
class definitions, dual typing that resource is preferred over asserting a
relationship between the classes.

Current graphs:

- [`shui.ttl`](shui.ttl) — opt-in alignments with the SHACL 1.2 User Interfaces
  Working Draft.
