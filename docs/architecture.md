# Architecture

## Four distinct layers

1. **Catalogue** — descriptive RDF about identity, versions, maturity, provenance, applicability, parameters, dependencies, compatibility, licensing and relationships. Catalogue records are not executable constraints.
2. **Modules** — immutable executable SHACL artefacts with declared feature tier and no implicit application targeting unless the contract says otherwise.
3. **Mappings** — consumer-controlled assertions mapping abstract roles (class, property, datatype, node kind or value scheme) to local terms. A mapping states a substitution purpose and direction; it is not an unrestricted ontological equivalence claim.
4. **Assembly** — deterministic selection, parameter binding, mapping, target injection and conflict checks producing a self-contained application shapes graph plus a manifest.

```text
catalogue record ----selects----> versioned module
       |                              |
       +---declares roles/params------+---specialise---+
                                                        v
local mapping + application config ----------------> assembled graph
                                                        |
                                                        v
                                             manifest + integration tests
```

## Core decisions

- **Pattern** is the public unit of discovery and documentation.
- **Module** is the versioned executable distribution unit.
- **Template** describes a module requiring bindings before execution; it is not directly imported.
- **Profile/assembly** is a resolved application-specific graph and manifest.
- Targets are application policy and normally injected at assembly time.
- Direct import is allowed only for a module explicitly marked `direct-import-safe`; templates never receive that mark.
- Mappings are allow-listed per role. Class, property, datatype, and concept-scheme substitutions have different proof obligations.
- Assembly does syntactic substitution only where declared; it does not run general OWL reasoning to discover replacements.
- Generated graphs use stable ordering, record source versions and digests, and remain reviewable without the generator.

## Closed-world behaviour

Closed shapes are not compositional by default: two modules may each reject properties permitted by the other. A closed-world pattern must expose its allowed-property set as an assembly input and be closed only after module composition. Closure is therefore usually an assembly phase, not a reusable module constraint.

## Dependency and conflict model

Dependencies are version-ranged pattern/module requirements with feature tiers. Releases resolve them to exact versions and digests. Conflicts may be declared explicitly; the assembler should also detect incompatible cardinalities, disjoint node-kind/datatype demands, unresolved roles, multiple closures, and unsupported engine features. Detection is advisory until a formal constraint-algebra subset is defined.

