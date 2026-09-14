# GPT Prompt Library

一个面向现代 GPT（当前优先 **GPT-6 Astra / GPT-5.6**）的高质量提示词仓库。

本仓库不追求堆积“你是一位世界级专家”式角色扮演 Prompt，而是尽量保存真正可观察、可复用、可验证的提示词约束：目标、受众、材料、结构、风格、事实边界、完成标准与自我编辑流程。

> Last updated: 2026-09-14

## 当前内容

- [`writing/GPT6_WRITING_PROMPTS.md`](writing/GPT6_WRITING_PROMPTS.md)：GPT 写作 Prompt 总库。覆盖 GPT-6 写作原则、自然写作、教科书、学术、技术、博客、小说、邮件、营销文案、风格模仿、自我编辑等。
- [`writing/GPT6_WRITING_SYSTEM_PROMPT.md`](writing/GPT6_WRITING_SYSTEM_PROMPT.md)：可直接复制使用的 GPT-6 总写作 System Prompt。

## 核心原则

相比旧式 Prompt：

```text
You are a world-class award-winning writer with 30 years of experience...
```

更推荐描述可观察的写作约束：

```text
读者是谁
→ 写作目标是什么
→ 哪些材料可信
→ 哪些内容不能自行假设
→ 信息应按什么关系展开
→ 语言应是什么样
→ 哪些表达应避免
→ 什么状态才算写完
```

现代 GPT 已经不太需要虚构资历来“进入角色”。更稳定的方式，是把任务定义、信息边界、文本结构和验收标准写清楚。

## 使用方式

最推荐三层组合：

1. 将 `GPT6_WRITING_SYSTEM_PROMPT.md` 作为长期写作规则。
2. 根据当前任务，从 `GPT6_WRITING_PROMPTS.md` 选择教科书 / 学术 / 技术 / 博客等专项 Prompt。
3. 完成初稿后，再使用“二次自我编辑 Prompt”进行独立 revision pass。

对于长文，不建议一次性要求“写 10000 字”。更稳定的流程是：

```text
Plan → Draft → Inspect → Revise → Fact-check → Finalize
```

## 来源原则

本仓库优先级大致为：

1. OpenAI 官方模型 / prompting / writing guidance
2. OpenAI Academy
3. OpenAI Developer Community
4. GitHub 高质量 Prompt repositories
5. Reddit / PromptEngineering 社区中的高质量实践
6. 其他近期 GPT-6 专门资料

社区 Prompt 不会无条件照搬。明显为了“骗 AI 检测器”而要求故意制造语法错误、随机矛盾、异常 perplexity / burstiness 的做法，不作为高质量正式写作默认策略。

## 维护方向

后续可继续加入：

- 科研论文各章节 Prompt（Abstract / Introduction / Related Work / Method / Experiments / Rebuttal）
- 教科书长期写作工作流
- Literature Review / Survey
- 技术文档与 API Documentation
- 中文正式写作
- 英文 Academic Writing
- Rewrite / Proofread / Copyedit
- Prompt evaluation / A-B testing
- 不同 GPT 模型的提示词差异

## License / attribution

Prompt 本身会尽量注明原始思想来源。对于来自社区或公开仓库的内容，本仓库优先进行归纳、改写和结构化，而非大段复制原文。
