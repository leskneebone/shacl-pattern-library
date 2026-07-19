# Experimental patterns

The initial set tests architecture rather than catalogue breadth:

1. [`labels/preferred-label-per-language`](labels/preferred-label-per-language/) tests language-sensitive uniqueness, multilingual messages and a SPARQL/Core portability boundary.
2. [`controlled-values/member-of-scheme`](controlled-values/member-of-scheme/) tests abstract property and concept-scheme roles, mapping safety and entailment assumptions.
3. [`dates/ordered-interval`](dates/ordered-interval/) tests cross-property comparison, datatype/timezone policy and report portability.

Each starts with a design brief. Executable modules and fixtures should be added only after their parameter and outcome contracts are reviewed.

