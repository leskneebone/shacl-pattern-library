# Value belongs to a concept scheme

**Question tested:** what does “controlled value” mean under different graph and entailment assumptions?

Abstract roles: constrained property and allowed scheme. Parameters: membership predicate (`skos:inScheme` by default), whether top-concept relations imply membership, named-graph scope, severity and target policy.

The pattern requires each value to be an IRI identified as a member of the configured scheme in the validation dataset. It does not assume that class membership, labels, broader/narrower paths, or an external vocabulary endpoint establish membership. If inferred membership is allowed, the entailment regime must be explicit and tested.

Fixtures must cover literal values, missing membership, membership in a different scheme, multiple schemes, unavailable external graphs, local property mapping and target isolation.

Direct import: no. Scheme and property roles must be bound; a specialised module may become direct-import-safe.

