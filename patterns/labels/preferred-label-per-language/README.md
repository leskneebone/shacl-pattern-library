# Preferred label per language

**Question tested:** can a pattern express “at most one preferred label for each language” without smuggling in an application language policy?

Abstract roles: focus-node class and label property. Parameters: whether untagged strings are allowed, whether plain and `xsd:string` count together, language-tag comparison/canonicalisation policy, severity, targets and message languages.

The common SKOS formulation is not expressible as a simple Core cardinality because uniqueness is grouped by language; the likely executable tier is SHACL-SPARQL. A separate Core building block can require `rdf:langString`, but must not claim the grouped uniqueness behaviour.

Fixtures must cover repeated same-language labels, different languages, case variants in language tags, untagged strings, invalid language tags as parser permits, and target isolation. Messages must not echo label lexical forms by default.

Direct import: no. This is an assembly-only template until roles, targets and language policy are bound.

