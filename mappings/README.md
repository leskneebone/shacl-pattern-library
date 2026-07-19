# Abstract-model mappings

Mappings are consumer-owned, directional substitution assertions used by assembly. They must identify the pattern role, local RDF term, substitution kind, scope, author, evidence and applicable pattern version range.

An RDF/OWL equivalence statement is neither required nor sufficient. A property suitable for a path role may still be unsafe for a cardinality or datatype role. The assembler must reject kind mismatches and undeclared substitutions. Mapping through arbitrary property paths or transformations is a future extension, not a basic equivalence.

