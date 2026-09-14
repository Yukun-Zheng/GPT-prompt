# Paper Experiments / 实验

<details>
<summary>Source & freshness</summary>

- Source: OpenAI Academy academic revision guidance; repository synthesis
- Status: official-derived + repository-synthesis
- Last verified: 2026-09-14
- Last updated: 2026-09-14
- Full references: [`../../90-research-来源研究/sources.md`](../../90-research-来源研究/sources.md)

</details>

## 中文版（直接复制）

```text
围绕“研究问题 / 假设”来撰写或修改 Experiments，而不是按照表格出现顺序逐项描述结果。

对于每个实验，明确说明：
1. 它要检验什么假设或研究问题
2. 当前实验设置如何尽量隔离这个问题
3. 使用什么指标，以及为什么这个指标适合回答该问题
4. 哪些 baseline、control 或 ablation 与这个问题真正相关
5. 实际观察到了什么结果
6. 这个结果支持什么结论
7. 这个结果不能支持什么更强的结论

要求：
- 区分实验设置、观测结果和解释
- 小幅数值差异不能在没有依据时被写成“显著改进”
- 当已有数据且确有必要时，报告随机种子、方差、置信区间或其他不确定性信息
- 区分 ablation、横向方法比较和 diagnostic analysis
- 不 cherry-pick 指标或只展示有利结果
- 除非实验真正识别了机制，否则不要仅根据最终性能反推内部机制
- 如果负结果或混合结果会影响论文 claim，应如实写出
- 所有数值 claim 必须能够追溯到表格、图、实验日志或其他已核验来源
- 明确指出实验结果的适用范围，不把某个 benchmark 上的结果直接扩大成普遍结论
```

## English version (copy directly)

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
