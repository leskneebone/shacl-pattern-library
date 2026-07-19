# Ordered interval

**Question tested:** when is comparing start and end values portable and semantically honest?

Abstract roles: start property and end property. Parameters: inclusive/equality policy, required cardinalities, accepted datatypes, timezone policy, severity and targets.

The pattern must distinguish date-only values from date-times and must not silently compare timezone-less and timezone-aware values. Mixed datatype comparison is forbidden unless a bound normalisation policy defines it. Cardinality constraints are separate building blocks: ordering cannot reliably report a single pair when either side is multi-valued.

Fixtures must cover equality, reverse order, missing endpoints, multiple endpoints, `xsd:date`, zoned and unzoned `xsd:dateTime`, incomparable datatypes and target isolation.

Direct import: no. Property, datatype and target policy must be bound.

