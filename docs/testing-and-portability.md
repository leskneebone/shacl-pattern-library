# Validation, testing and portability

## Feature tiers

- **Core**: SHACL Core only, no required entailment.
- **Core+RDFS**: Core with a declared RDFS entailment expectation.
- **SPARQL**: SHACL-SPARQL constraints with query and complexity review.
- **AF**: SHACL Advanced Features, with each required feature named.
- **Engine-specific**: implementation extensions; never advertised as portable.

Portability is claimed per module and engine/version matrix, not for the library as a whole.

## Minimum test suite

Each pattern has positive, negative, zero/one/many boundary, malformed-term, language/datatype, mapping, target-isolation and dependency tests where applicable. Each test fixes the data graph, shapes graph, configuration, entailment, expected conformance and expected result signatures.

Exact report graph equality is not generally portable. Core tests compare conformance plus normalised tuples of focus node, result path, source constraint component, severity and (when stable) value. Message wording, blank-node identifiers and result ordering are informative unless a pattern contract makes them application requirements.

## Proposed maturity gates

| Maturity | Minimum evidence |
|---|---|
| Experimental | Pattern contract draft, syntax-valid RDF, examples and known limitations |
| Candidate | Complete tests, security/performance review, two independent conforming engines for claimed portable tiers, unresolved issues published |
| Stable | Candidate feedback resolved, frozen semantics, migration/version plan, reproducible signed release archive and steward approval |
| Deprecated | Reason, replacement or alternative, migration guidance, continued identifier resolution |

## Operational tests

Use bounded adversarial fixtures for long paths, large value sets, recursion, expensive regexes and SPARQL joins. Record hardware-independent budgets where possible (dataset size, result count, query shape) and measured budgets as evidence, not universal guarantees. Validation over untrusted data should support time, memory and result-count limits.
