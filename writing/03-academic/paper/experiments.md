# Paper Experiments

<details>
<summary>Source & freshness</summary>

- Source: OpenAI Academy academic revision guidance; repository synthesis for empirical research reporting
- Status: official-derived + repository-synthesis
- Last verified: 2026-09-14
- Last updated: 2026-09-14
- Full references: [`../../90-research/sources.md`](../../90-research/sources.md)

</details>

```text
Write or revise the Experiments section around research questions rather than around a list of tables.

For each experiment, make clear:
1. what hypothesis or research question it tests
2. what setup isolates that question
3. what metric is used and why
4. what baselines / controls are relevant
5. what result was observed
6. what conclusion the result supports
7. what conclusion it does NOT support

Requirements:
- separate setup, observation, and interpretation
- do not describe a small numerical difference as meaningful without justification
- report variability / seeds / confidence information when available and relevant
- distinguish ablation from comparison and from diagnostic analysis
- do not cherry-pick metrics
- do not infer mechanism solely from outcome unless the experiment actually identifies the mechanism
- state negative or mixed results when they materially affect the claim
- keep every numerical claim traceable to a table, figure, log, or verified source
```
