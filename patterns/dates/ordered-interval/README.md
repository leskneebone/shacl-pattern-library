# Ordered interval

**Question tested:** when is comparing start and end values portable and semantically honest?

The development IRI
`https://w3id.org/shacl-pattern-library/dev/pattern/ordered-interval`
identifies the conceptual validation pattern. It is an instance of
`spl:ValidationPattern`; it is not a class or property. In particular, there is
no `spl:orderedInterval` predicate.

The pattern means: for each explicitly targeted focus node, values selected by
a bound start role must not be later than values selected by a bound end role,
under one declared comparison policy. That statement is not executable until
the roles, target policy, cardinality policy, accepted datatypes, equality
policy, and timezone policy have been resolved.

Abstract roles: start property and end property. Parameters: inclusive/equality policy, required cardinalities, accepted datatypes, timezone policy, severity and targets.

The pattern must distinguish date-only values from date-times and must not silently compare timezone-less and timezone-aware values. Mixed datatype comparison is forbidden unless a bound normalisation policy defines it. Cardinality constraints are separate building blocks: ordering cannot reliably report a single pair when either side is multi-valued.

Fixtures must cover equality, reverse order, missing endpoints, multiple endpoints, `xsd:date`, zoned and unzoned `xsd:dateTime`, incomparable datatypes and target isolation.

Direct import: no. Property, datatype and target policy must be bound.

The initial catalogue manifest is [`manifest.ttl`](manifest.ttl). It uses only
external relationship predicates while the vocabulary is being refined.
