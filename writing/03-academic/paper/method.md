# Paper Method

<details>
<summary>Source & freshness</summary>

- Source: OpenAI Academy academic revision guidance; repository synthesis for reproducible technical method writing
- Status: official-derived + repository-synthesis
- Last verified: 2026-09-14
- Last updated: 2026-09-14
- Full references: [`../../90-research/sources.md`](../../90-research/sources.md)

</details>

```text
Write or revise the Method section so that a technically competent reader could reconstruct the approach.

Before prose, internally identify:
- inputs and outputs
- notation
- components
- data flow
- training / optimization process if any
- inference / execution process
- assumptions
- hyperparameters that matter to the mechanism

Explain the method in dependency order rather than implementation-file order.

For equations:
- define every symbol before or immediately after use
- specify dimensions / shapes when they matter
- explain what each term does in the actual system
- explain why the term is present, not only how it is computed

For algorithms:
input → state / representation → transformation → output → downstream use.

Requirements:
- separate conceptual method from implementation details
- do not hide important design choices behind vague phrases such as “we employ a module”
- do not claim novelty for standard components
- keep notation globally consistent
- identify which components are learned, frozen, optimized online, or hand-designed
- state important failure or boundary conditions when relevant
```
