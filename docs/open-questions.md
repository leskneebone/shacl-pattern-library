# Open questions

The architectural experiments should answer these before the catalogue expands:

- Can a useful substitution vocabulary remain small and safe, or does mapping require pattern-specific code?
- Which constraint conflicts can be detected soundly before validation?
- Can direct-import safety be defined strongly enough to be useful?
- What is the canonical normal form and digest process for executable RDF?
- Which two independent engines form the initial Core portability gate?
- Should catalogue terms reuse PROF, DCAT, DCTERMS, ADMS, SPDX or OWL, and where is a small local vocabulary justified?
- How should ValPub requirements map to pattern lineages, versions and distributions?
- What translation review and fallback guarantees are feasible?
- Does CC0 give contributors and institutional adopters sufficient clarity, or should code and documentation use separate permissive licences?
- What namespace steward and transfer mechanism can meet the persistence requirements?
- What assembly language is minimal, deterministic and inspectable?

Decisions belong in dated records under `docs/decisions/`; unresolved questions must not be disguised as implementation conventions.

