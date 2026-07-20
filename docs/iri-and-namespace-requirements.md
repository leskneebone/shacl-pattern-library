# IRI and namespace requirements

No permanent namespace is selected. Examples use `https://w3id.org/shacl-pattern-catalogue/dev/` solely as an unmistakably provisional development base; no redirect has been registered.

## Resources requiring IRIs

Patterns, released pattern versions, executable module versions, abstract roles, parameters, maturity concepts, compatibility tiers, mapping assertions, generated assembly manifests and released profiles need IRIs when they must be cited or related across graphs. Test cases and individual constraints receive IRIs when reports, provenance or overrides must address them; otherwise local blank nodes may be acceptable.

## Required properties of a future authority

- organisational neutrality and documented stewardship succession;
- HTTPS dereferenceability with content negotiation;
- persistence independent of source hosting and build tooling;
- control shared by more than one accountable custodian;
- preservation of retired identifiers and machine-readable tombstones;
- archived release artefacts and recoverable redirects;
- clear incident, compromise and namespace-transfer procedures.

## Identifier policy to test

- A version-independent pattern IRI identifies the conceptual lineage.
- An immutable version IRI identifies one released normative pattern description.
- Executable artefact IRIs are version-specific and content-addressed in manifests.
- Version-independent IRIs may resolve to the current recommended version but must not be imported as mutable executable content.
- Renaming creates an alias record; semantic replacement uses `replacedBy`; retirement never recycles an IRI.
- Patch releases cannot alter validation outcomes for the same RDF dataset, declared entailment and configuration. Outcome changes require at least a minor version; incompatible normative semantic changes require a major version.

Before a stable release, test persistence, redirect, backup, domain-loss and governance-transfer scenarios and replace the development base through an explicit migration decision.
