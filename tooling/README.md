# Assembly tooling

The intended assembler consumes exact pattern versions, a local mapping graph, explicit targets and parameters, then emits a self-contained shapes graph and manifest. Output must be deterministic and reviewable. It must not fetch mutable dependencies during assembly, discover semantic equivalence through general reasoning, or conceal unsupported features.

No implementation is justified until a hand-worked assembly for each experiment establishes the minimal input model.

