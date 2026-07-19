# 0002 — Reuse before defining local properties

Status: provisional  
Date: 2026-07-19

The first SPL ontology defines necessary local classes but no local properties.
Pattern manifests initially reuse relationships from DCAT 3, DCTERMS, ADMS,
PROV-O, SHACL, OWL, and other established vocabularies where their published
definitions fit.

A local property may be proposed only after:

1. its required meaning, domain expectations, range expectations, and
   entailment consequences are written down;
2. established source vocabularies and vocabulary registries are searched;
3. near matches are recorded with the reason each is too broad, too narrow, or
   otherwise incompatible;
4. at least two pattern manifests demonstrate that the relationship is part of
   the reusable architecture rather than one pattern's implementation detail.

This policy applies to properties, not to local classes required to identify
the project's own catalogue resources. A familiar local name does not establish
equivalence with an external term. Conversely, a broad external property should
not be retained merely to avoid minting a term when it prevents consumers from
understanding an operationally important distinction.
