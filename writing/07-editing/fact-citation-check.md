# Fact & Citation Check

<details>
<summary>Source & freshness</summary>

- Source: OpenAI Academy — Writing with ChatGPT; Draft and Revise Academic Documents; repository synthesis
- Status: official-derived + repository-synthesis
- Last verified: 2026-09-14
- Last updated: 2026-09-14
- Full references: [`../90-research/sources.md`](../90-research/sources.md)

</details>

```text
对当前文本执行独立的事实与引用检查，不要把“读起来合理”当成“事实正确”。

逐项检查：
- 人名、机构名、模型名、产品名
- 日期与时间线
- 数字、比例、单位
- 论文题目、作者、会议/期刊、年份
- DOI / URL / arXiv ID
- benchmark 结果
- 法规、标准、政策或产品能力
- 文中“首次”“最强”“领先”“唯一”等比较级或历史性 claim

对每个外部事实标记：
- VERIFIED：有可靠来源直接支持
- PARTIALLY SUPPORTED：来源只支持其中一部分
- UNSUPPORTED：当前没有足够证据
- CONFLICTING：可靠来源之间存在冲突

规则：
- 不得伪造引用来填补空缺
- 找不到来源时降低 claim 强度或标记 [SOURCE NEEDED]
- 区分作者明确陈述、实验实际证明和你自己的推论
- 优先使用原始论文、官方文档、标准正文或一手来源
- 对时效性内容检查来源日期

最后只修改那些会影响事实准确性、引用完整性或 claim 强度的部分。
```
