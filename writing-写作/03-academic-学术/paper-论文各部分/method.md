# Paper Method / 方法

<details>
<summary>Source & freshness</summary>

- Source: OpenAI Academy academic revision guidance; repository synthesis
- Status: official-derived + repository-synthesis
- Last verified: 2026-09-14
- Last updated: 2026-09-14
- Full references: [`../../90-research/sources.md`](../../90-research/sources.md)

</details>

## 中文版（直接复制）

```text
撰写或修改论文 Method，使一个具备相应技术背景的读者能够据此重建方法的核心过程，而不是只能得到模糊的高层描述。

正式写正文前，先在内部明确：
- 输入是什么
- 输出是什么
- 使用哪些符号
- 包含哪些组件
- 数据如何在组件之间流动
- 如果存在训练 / 优化，具体如何进行
- 推理 / 执行阶段如何运行
- 方法依赖哪些假设
- 哪些超参数会实质影响机制

按概念和依赖关系解释方法，而不是按照代码文件或工程目录顺序介绍。

对于公式：
- 每个符号必须在使用前或紧邻位置定义
- 当维度 / shape 重要时明确写出
- 解释每一项在实际系统中对应什么
- 不只说明“怎么算”，还要说明“为什么需要这一项”

对于算法，尽量按以下数据流说明：
输入 → 状态 / 表示 → 变换 → 输出 → 下游如何使用。

要求：
- 区分概念方法与实现细节
- 不要用“we employ a module”之类模糊短语隐藏关键设计
- 不要把标准组件包装成创新
- 全文符号必须一致
- 明确哪些组件是 learned、frozen、online optimized 或 hand-designed
- 必要时说明重要失败条件、适用边界和假设
- 如果存在张量，关键位置尽量给出 shape 及 shape 变化
```

## English version (copy directly)

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
