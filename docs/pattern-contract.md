# Pattern contract

Every published pattern package must state:

1. stable pattern identifier and immutable version identifier;
2. title, description, rationale, intended users, applicability and non-goals;
3. whether it is abstract, directly importable, or assembly-only;
4. abstract roles, parameters, defaults, legal values and substitution rules;
5. targets, graph/dataset assumptions and entailment regime;
6. executable modules and required SHACL feature tier;
7. dependencies, incompatibilities and tested engine versions;
8. conforming, non-conforming and boundary examples with expected outcomes;
9. normative constraint meaning and informative multilingual messages;
10. performance, denial-of-service, privacy and report-disclosure considerations;
11. authorship, provenance, licence, maturity, creation/modification dates;
12. semantic version, replacement/deprecation and migration information;
13. customisation points, forbidden edits and direct-import safety;
14. machine-readable manifest and artefact digest.

The constraint meaning is normative. Labels, descriptions, examples and messages explain it but cannot silently change it. A missing requested language falls back in this order: exact language tag, primary language subtag, project default language (initially English), then an untagged message. Engines may choose differently, so applications needing deterministic language should select messages during assembly.

