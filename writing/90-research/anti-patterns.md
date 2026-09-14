# Writing Prompt Anti-patterns

这些模式在社区 Prompt 中很常见，但不应作为高质量正式写作的默认策略。

## 1. 虚构资历代替任务定义

```text
You are a world-class award-winning writer with 30 years of experience...
```

问题：没有说明受众、事实边界、结构、材料和完成标准。现代模型通常更需要可观察约束，而不是虚构履历。

## 2. Humanizer / Detector Optimization

```text
maximize perplexity
maximize burstiness
insert deliberate grammatical errors
add random contradictions
introduce irrelevant tangents
beat GPTZero / Turnitin
```

问题：把“自然写作”错误等同于随机噪声。真正有价值的通常只是句长变化和句法结构变化。

## 3. 形容词堆叠

```text
engaging, compelling, insightful, powerful, captivating, revolutionary...
```

问题：这些词没有定义可观察的写作行为，很容易反过来诱发营销腔和 AI 套话。

## 4. 一次要求完成全部长文

```text
Write a perfect 20,000-word textbook chapter in one response.
```

问题：规划、起草、验证、修订被混在一次生成中，长程一致性与事实核验更难控制。

更推荐：

```text
Plan → Draft → Inspect → Revise → Fact-check → Finalize
```

## 5. “不要像 AI”但不给标准

```text
Write like a human. Do not sound AI-generated.
```

问题：不可操作。应改成可观察规则，例如减少元话语、机械总结、固定对比句式、重复论点和无信息形容词。

## 6. 无条件禁止某些词

绝对禁词表容易让模型为了绕开词汇而产生更怪的表达。更好的判断标准是：该表达是否增加信息、是否符合当前语境、是否重复成为模板。

## 7. 把同一 Prompt 用于所有文体

论文 Method、邮件、小说、教材和营销文案的成功标准完全不同。仓库因此按任务分类，而不是维护一个不断膨胀的“万能 Prompt”。
