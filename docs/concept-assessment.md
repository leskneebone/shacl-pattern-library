# Concept assessment and risk register

The concept is useful, but a collection of generic shapes is the wrong centre of gravity. SHACL constraints bind validation logic to targets, paths, graph topology, entailment, engine behaviour, and operational policy. Reuse should therefore package a pattern contract and evidence around executable material.

The smallest useful **catalogued** unit is a pattern. Its smallest executable unit may be a constraint component or shape, and its deployable unit is a module. These units should not be conflated.

## Principal risks

| Risk | Consequence | Initial control |
|---|---|---|
| False equivalence | Local terms are substituted although validation semantics differ | Typed, directional mappings with explicit admissibility and tests; never infer substitution from labels or `owl:equivalent*` alone |
| Hidden targeting | Import unexpectedly validates more nodes | Reusable modules omit ambient targets by default; assembly adds targets explicitly |
| Constraint collision | Independently valid patterns create an impossible profile | Assembly checks dependency versions, parameter domains, duplicate paths and known incompatibilities; final graph receives integration tests |
| Version drift | An import changes behaviour without consumer action | Immutable versioned artefacts, lock data and semantic-version policy |
| Engine divergence | Results or failures differ | Capability tiers, multiple-engine evidence and explicit report comparison level |
| Unsafe complexity | SPARQL/path patterns exhaust resources | Complexity notes, bounded fixtures, time/memory budgets and untrusted-data threat review |
| Information disclosure | Messages/reports expose sensitive values or topology | Message review, redaction guidance, minimal default messages and operational policy |
| Translation drift | Localised messages assert different rules | One normative constraint meaning; translations reviewed and fallback declared |
| Catalogue/executable mismatch | Metadata overstates actual behaviour | Machine-checkable links, release gates and generated inventory tests |
| Premature authority | Development IRIs are mistaken for stable standards | Conspicuous `/dev/` namespace, maturity labels and disclaimer |
| Supply-chain dependency | Transitive import changes or disappears | Vendoring/locking guidance, digests and dependency closure in releases |
| Licence/provenance contamination | Reuse rights are unclear | Per-resource provenance, contribution attestation and compatibility review |

## Missing requirements now made explicit

Accessibility of documentation, deterministic builds, canonical artefact digests, blank-node policy, RDF dataset/graph assumptions, entailment regime, severity policy, validation report comparison rules, engine capability discovery, resource budgets, threat modelling, dependency locking, changelog/migration guidance, translation governance, offline operation, and reproducible release archives all belong in the design.
