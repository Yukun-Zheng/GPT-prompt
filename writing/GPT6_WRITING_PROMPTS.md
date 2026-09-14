# GPT-6 Writing Prompt Library

> 面向 GPT-6 Astra / 现代 GPT 的写作提示词母库  
> Last updated: 2026-09-14

本文档不是“万能咒语合集”，而是一套可组合的写作控制模块。核心思想是：**少依赖虚构角色，多依赖可观察的写作约束。**

---

## 0. 总原则：现代 GPT 写作 Prompt 应该控制什么

一个高质量写作 Prompt，最好明确以下八类信息：

1. **Goal**：最终文本要完成什么任务。
2. **Audience**：写给谁，他们已经知道什么。
3. **Grounding**：哪些事实、材料、文献、数据可以使用。
4. **Scope**：哪些必须写，哪些不能擅自补。
5. **Structure**：信息按什么认知或论证关系展开。
6. **Style**：语域、句式、段落、术语和格式偏好。
7. **Anti-patterns**：明确禁止的模板化表达。
8. **Definition of done**：什么状态才算真正写完。

相比：

```text
You are a world-class writer with 30 years of experience.
```

更推荐：

```text
目标 → 受众 → 材料 → 边界 → 结构 → 风格 → 禁止项 → 验收标准
```

---

# 1. GPT-6 基础写作规则

适合挂在所有长文任务前，作为默认约束。

```text
【GPT-6 基础写作规则】

默认以连贯的自然段写作，每个段落围绕一个主要思想展开。

只有当信息天然属于并列、步骤、枚举或比较关系时才使用列表或表格。
不要为了“清晰”而把正常文章拆成大量标题、项目符号和碎片。

优先使用：
- 熟悉而准确的词
- 具体名词
- 精确动词
- 主动语态
- 直接陈述
- 能真正解释问题的具体例子

文章应尽早进入核心内容。
让下一句话自然继承上一句话的信息，而不是依赖模板化转折词连接。

避免机械的 AI 套话、空洞评价和没有信息量的过渡。
不要反复使用“值得注意的是”“重要的是”“总而言之”“简单来说”等表达。

不要为了制造强调感而频繁使用：
“不是 X，而是 Y”
“真正重要的不是 X，而是 Y”
“问题是什么？答案是……”
等固定修辞结构。

不要发明没有必要的概念标签或连字符复合形容词。

结尾应结束论证或自然落点，而不是机械地重复全文内容。
```

---

# 2. 通用写作任务母 Prompt

适合文章、报告、说明文、章节、长回答等。

```text
# WRITING TASK

## 目标
我要最终得到：
[文章 / 论文段落 / 教科书章节 / 博客 / 报告 / 邮件 / 说明文]

文章真正要完成的任务是：
[读者读完后应该知道、理解、相信或能够做到什么]

## 受众
目标读者：
[背景知识、领域、阅读目的]

假定他们已经知道：
[...]

不要假定他们知道：
[...]

## 内容来源
主要依据：
[我的笔记 / 文献 / 网页 / 数据 / 附件 / 已知事实]

不得自行捏造缺失事实、文献、数字或引用。

## 核心内容
必须覆盖：
1. [...]
2. [...]
3. [...]

可以根据逻辑需要调整顺序。

## 深度
不要只介绍“是什么”。
必要时解释：
- 为什么
- 如何工作
- 各部分如何连接
- 前提是什么
- 什么时候成立
- 什么时候失效
- 与相关概念有什么区别
- 一个具体例子中发生了什么

## 写作风格
以自然、成熟、连贯的人类书面语言写作。

优先使用自然段。
一句话只承担它能够承担的信息量。
避免空洞修辞、企业黑话和 AI 套话。

专业内容可以使用领域术语，但第一次出现的重要术语应自然解释。

## 结构
文章应具有明确的信息推进关系，例如：

问题/背景
→ 核心思想
→ 机制或论证
→ 具体展开
→ 例子或证据
→ 推论或意义

不要机械套用这些标题。
应根据内容本身形成自然结构。

## 自主性
如果只是次要细节缺失，根据上下文作合理选择并继续写作。
只有当缺失信息会实质性改变文章结论时才提出问题。

## 完成标准
完成后自行检查：
- 是否真正回答了主题
- 是否存在重复段落
- 是否存在没有作用的句子
- 是否存在空泛结论
- 是否偷换概念
- 是否新增了材料中没有依据的事实
- 是否出现明显 AI 模板腔

然后输出最终稿。
```

---

# 3. 自然写作 / 去模板化 Prompt

目的不是“骗 AI detector”，而是减少模板腔、空话和机械节奏。

```text
【自然写作规则】

不要试图“写得像 AI 想象中的优秀文章”。
像一个真正理解这个问题的人在认真向另一个人解释。

优先清楚，其次才是漂亮。

1. 使用准确、自然的词。
   不为了显得高级而主动替换成更生僻的词。

2. 控制句子节奏。
   短句、中等长度句和必要的长句自然混合。
   不要让每句话拥有相同结构和长度。

3. 删除填充句。
   如果一句话既没有增加事实、解释、论证、例子，也没有推动叙述，就删除。

4. 不使用营销式夸张。
   避免 revolutionary、game-changing、transformative、unlock、elevate 等没有证据支撑的词。

5. 少使用元话语。
   不要频繁告诉读者“接下来我们将……”“值得注意的是……”“重要的是……”。

6. 使用具体例子代替抽象赞美。

7. 不要假装热情。
   不需要不断使用“令人兴奋”“非常强大”“极其重要”等词。

8. 允许自然的不对称。
   段落不必等长，句式不必整齐，但不要故意制造语法错误。

9. 如果一个专业术语比日常替代说法更准确，就使用专业术语。
   “简单”不等于“幼稚”。

10. 写完后删除任何明显像模板自动生成的句子。
```

## 不推荐的“Humanizer”策略

以下策略在社区中很常见，但不建议用于正式写作：

```text
maximize perplexity
maximize burstiness
insert deliberate grammatical errors
add random contradictions
introduce irrelevant tangents
beat GPTZero / Turnitin
```

真正有价值的部分通常只有：

```text
让句长自然变化。
避免所有句子采用相同的语法模板。
```

---

# 4. Style Profile：模仿用户自己的写作风格

比“像我一样写”更稳定。

```text
下面是我本人写的若干文本。

不要先生成新文章。

第一步，只分析我的稳定写作特征。

分别分析：
1. 句子平均长度及变化范围
2. 长句与短句如何交替
3. 段落通常如何展开
4. 常用连接方式
5. 是否喜欢显式总结
6. 抽象概念与具体例子的比例
7. 专业术语密度
8. 第一/第二/第三人称使用方式
9. 常用动词和形容词类型
10. 标点偏好
11. 修辞习惯
12. 开头方式
13. 结尾方式
14. 我的文章最容易被识别出的特征
15. 我明显不会使用的表达

把这些总结成一个“Style Profile”。

然后，当我给出新的写作任务时：

保留新任务的事实和观点，
但使用 Style Profile 中稳定而可迁移的特征。

不要复制原文中的具体句子。
不要为了模仿而重复我的偶然错误。
优先模仿深层结构、节奏、语域和论证方式。
```

---

# 5. 教科书 / 专著长文 Prompt

适合持续数十章甚至数百章的知识体系写作。

```text
你正在参与一本真正需要长期使用的专业教材写作。

不要把任务理解成“生成一篇长文章”。
你的工作是构建一个连续、可维护的知识体系。

每章写作前先确定：

1. 本章在整本书中的作用
2. 本章读者已有的知识
3. 本章需要建立的新概念
4. 这些概念之间的依赖关系
5. 本章结束时读者应该能够做到什么
6. 哪些内容将在后续章节继续使用

正文遵循“认知依赖关系”而不是百科词条排列。

一个概念出现时：
先让读者理解为什么需要它，
再给定义，
再解释内部机制，
再给最小例子，
再逐步增加复杂度，
最后连接到真实系统。

数学内容不要只给公式。
解释：
- 变量是什么
- shape 是什么
- 每一步发生了什么
- 为什么这样定义
- 它和实际系统中的哪一步对应

算法内容尽量给：
输入
→ 中间状态
→ 输出
→ 数据流
→ 失败情况。

不要每节都用“首先……其次……最后……”这样的模板。
不要每一节末尾机械加入总结。

重要概念可以重复出现，但第二次出现必须增加新的理解，而不是换句话复述。

任何事实、历史事件、论文结论或数字，如果来源可以获得，应给来源。

最终目标不是写得长，而是让读者真正从零建立完整认知模型。
```

---

# 6. 学术写作 Prompt

适合论文、论文段落、课程论文、研究报告 revision。

```text
你现在充当学术编辑，而不是论文代写者。

保留：
- 我的原始论点
- 我的事实主张
- 我的证据
- 我的立场

不要擅自增加新的学术结论。

检查：

1. 论点是否清晰
2. 每个论点是否得到证据支持
3. evidence 与 interpretation 是否混在一起
4. 是否存在逻辑跳跃
5. 是否存在重复论证
6. topic sentence 是否承担了正确功能
7. 段落之间是否存在真正的逻辑关系
8. 术语是否一致
9. 是否存在夸大 claim
10. 是否存在需要引用但没有引用的地方

对于每个需要修改的段落给：

A. 最小修改版
尽可能保留原句。

B. 深度修改版
优化论证结构。

C. 修改原因
只解释真正影响学术质量的修改。

不得伪造引用。
不知道来源时明确标记 [SOURCE NEEDED]。
```

---

# 7. Academic English 专项 Prompt

```text
Rewrite the passage as clear academic English without making it sound artificially ornate.

Preserve the original technical meaning, claims, evidence, uncertainty, and scope.

Prioritize:
- precise terminology
- explicit logical relationships
- economical sentences
- consistent technical terms
- calibrated claims
- appropriate academic register

Do not:
- inflate ordinary claims
- add unsupported novelty claims
- replace precise technical terms with vague synonyms
- overuse “novel”, “significant”, “remarkable”, “crucial”, or “important”
- introduce citations that were not provided
- convert every sentence into passive voice

Where the original logic is ambiguous, flag the ambiguity instead of silently inventing a stronger claim.
```

---

# 8. 技术写作 Prompt

```text
以技术作者的方式写作。

准确性优先于修辞效果。

不要为了“通俗”而把正式技术概念替换成不准确的生活化说法。

对于重要机制，依次回答：

它是什么？
它解决什么问题？
输入是什么？
内部发生什么？
输出是什么？
依赖什么？
失败时会怎样？
为什么不用更直接的方法？

如果存在数据结构或张量：
明确写出 shape。

如果存在系统：
明确写出组件及数据流。

如果存在算法：
给出一个具体输入，从头追踪到输出。

术语第一次出现时自然定义。
之后直接使用正式术语。

使用图、表、列表的唯一理由是它们比段落更适合表达当前信息。
不要为了显得“技术化”而过度结构化。
```

---

# 9. 机制 / 数据流优先的技术解释 Prompt

适合机器学习、机器人、系统、编译器等。

```text
不要先堆公式或概念定义。

先画出系统中的角色和数据流：

输入是什么
→ 经过哪个模块
→ shape / datatype 如何变化
→ 模块做了什么操作
→ 输出给谁
→ 下一步如何使用

如果有多个并行分支，先明确每个分支各自负责什么，再解释它们何时交互。

然后再给数学定义，并让每个公式中的符号都能回到前面的数据流图中找到对应物。

对于每个关键张量，尽可能明确：
- shape
- 每一维代表什么
- 在 batch / time / token / joint / camera 等维度上如何变化

最后用一个足够小、可以手工跟踪的具体例子，从输入完整走到输出。
```

---

# 10. Blog / 科普文章 Prompt

```text
主题：
[...]

读者：
[...]

读者打开这篇文章最可能想解决的问题：
[...]

先确定读者最关心的 5 个真实问题。
然后围绕这些问题组织文章。

开头不要写泛化背景。
尽快回答主要问题。

每个章节必须增加新信息。
使用具体案例解释抽象概念。

只有真正有比较需求时才使用表格。
不要为了 SEO 重复关键词。
不要加入为了增加长度而存在的 FAQ。
不要重复总结前文。

文章结束在一个有实际信息价值的结论、判断或行动建议上。
```

---

# 11. 营销 / 产品文案 Prompt

```text
写营销文案，但不要写成“营销腔”。

先明确：

受众现在是什么状态？
他们真正的问题是什么？
产品具体解决哪一个问题？
有什么能够证明的差异？
希望他们下一步做什么？

正文优先：
具体事实
→ 对用户意味着什么
→ 实际收益
→ 下一步。

不要使用没有证据的：
revolutionary
 game-changing
 unprecedented
 world-class
 next-generation
 transformative
等词。

不要把普通功能包装成巨大愿景。
如果产品价值很简单，就简单地说。
```

---

# 12. 邮件 Prompt

```text
根据以下情况写邮件。

对象：
[...]

关系：
[...]

背景：
[...]

我真正希望对方做：
[...]

语气：
自然、专业、礼貌，但不要过度客套。

要求：
尽快进入主题。
不要使用企业套话。
不要重复背景。
不要过度道歉。
不要用很长的开场寒暄。
明确说明下一步。
不超过 [...] 字。
```

---

# 13. 小说 / 叙事类 Prompt

```text
写成真正的连续叙事，而不是“电影预告片式”文字。

不要依靠：
- 大量一句一段
- 破折号制造虚假戏剧性
- 人物反复颤抖、屏息、心跳加快
- 每个动作后立刻解释人物情绪
- 频繁 cliffhanger
- 过度诗意比喻

让情绪主要来自：
人物的选择，
没有说出口的信息，
行为之间的矛盾，
环境中的具体细节，
以及事件本身的后果。

人物心理可以复杂，但不要把所有心理活动解释给读者。

段落允许充分发展。
场景之间需要有真正的因果连续性。
```

---

# 14. 编辑诊断 Prompt

比“帮我润色一下”更稳定。

```text
不要直接重写。

先作为编辑阅读全文。

找出：
- 可以删除而不损失信息的句子
- 重复表达
- 抽象但没有内容的句子
- 逻辑跳跃
- 过度解释
- 信息出现顺序错误
- 不符合全文语域的词
- AI 模板句
- 不必要的总结
- 可以用具体例子替代的抽象描述

然后提出结构修改。

只有完成诊断后再生成修改稿。

修改时优先保留原作者已经写得好的句子。
不要为了证明自己修改过而重写所有内容。
```

---

# 15. 二次自我编辑 Prompt

建议与初稿生成分成两个独立 pass。

```text
现在不要继续扩展内容。

以编辑身份重新阅读刚才的文本。

逐句检查以下问题：

1. 这句话是否增加了信息？
2. 是否只是上一句的换一种说法？
3. 是否使用了模板化 AI 表达？
4. 能否用更具体的名词或动词表达？
5. 是否存在没有依据的评价性形容词？
6. 是否在告诉读者“这很重要”，却没有通过内容证明？
7. 是否为了转折而转折？
8. 是否存在不必要的总结？
9. 是否存在过度解释？
10. 段落顺序是否符合认知或论证顺序？

删除没有作用的句子。
然后重新调整句子与段落顺序。

不要改变核心事实和论点。

最后只输出修订后的正文。
```

---

# 16. 事实与引用守门 Prompt

适合调研、论文、教材和技术文档。

```text
把“语言流畅”和“事实可信”分开处理。

对全文中的每一个外部事实主张进行检查：

- 数字
- 日期
- 人名 / 机构
- 历史事件
- 论文结论
- benchmark 结果
- 法规 / 标准
- 产品能力
- 当前状态

如果有可靠来源，给出来源。
如果没有来源，不要把猜测写成事实。
如果事实存在争议，标记争议和不同口径。
如果信息可能随时间变化，优先核验最新状态。

不要伪造 DOI、URL、作者、会议、论文题目或统计数字。
```

---

# 17. 从粗笔记生成正式正文 Prompt

```text
下面是我的粗笔记。

你的工作不是逐条扩写，而是先恢复这些笔记背后的逻辑结构。

第一步：识别
- 核心论点
- 支撑事实
- 推理链
- 例子
- 未解决的问题
- 重复信息

第二步：根据逻辑关系重新排序。

第三步：写成连续正文。

要求：
- 不遗漏关键观点
- 不把暂定想法写成确定事实
- 不凭空补充论点
- 不保留笔记式碎片感
- 不强制一条笔记对应一个段落

如果多个笔记其实属于同一论点，应合并成一个完整段落。
```

---

# 18. 从文献生成 Related Work Prompt

```text
根据给定文献写 Related Work。

不要按“论文 A 做了什么，论文 B 做了什么，论文 C 做了什么”的文献流水账组织。

先识别这个领域中真正不同的技术路线、问题定义或假设。

按方法族 / 问题族组织：

路线 A：共同核心假设是什么？
代表工作有哪些？
解决了什么？
仍受什么限制？

路线 B：同理。

然后明确本文与这些路线之间的关系。

不要为了制造 novelty 而贬低已有工作。
不要把未验证的差异写成确定优势。
不要伪造引用。
```

---

# 19. Paper Introduction Prompt

```text
写论文 Introduction 时，完成一条完整论证链：

1. 问题为什么真实存在且值得研究
2. 现有路线主要如何解决
3. 真正尚未解决的技术缺口是什么
4. 为什么这个缺口不是一句话就能绕开的
5. 本文核心思想是什么
6. 为什么这个思想有可能解决该缺口
7. 本文具体贡献是什么

不要用夸张的宏大背景拖长开头。
不要为了凑 contribution 数量把一个贡献拆成三条。
不要声称“首次”除非已经系统核验。
不要提前把 experiments 的结果写成超出证据的结论。
```

---

# 20. Paper Method Prompt

```text
Method 的目标不是让文章“看起来数学”，而是让别人能够准确复现方法。

按以下顺序组织：

1. Problem formulation
2. Inputs / outputs
3. Symbols and dimensions
4. Overall pipeline
5. Each component
6. Training / optimization
7. Inference / execution
8. Complexity or implementation details when relevant

任何公式都必须说明：
- 每个变量代表什么
- shape / domain 是什么
- 公式在系统中对应哪一步
- 为什么需要这一项

不要先抛大量符号再解释。
先让读者知道整个系统在做什么，再进入局部数学。
```

---

# 21. Paper Experiments Prompt

```text
Experiments 不只是报告数字，而是验证论文中的具体 claim。

先列出论文最重要的 claims。
然后为每个 claim 指定至少一个对应实验。

实验章节应回答：
- 与谁比较
- 为什么这些 baseline 合理
- 控制了哪些变量
- 使用什么数据 / task / metric
- 主结果说明什么
- ablation 验证哪一个机制
- failure case 暴露什么边界
- 结果是否具有统计可靠性

不要把“数字更高”自动等价成“机制解释正确”。
区分 empirical performance 与 causal explanation。
```

---

# 22. Reviewer / Rebuttal Prompt

```text
阅读 reviewer comment 后，不要立即辩解。

先把每条评论分类：
- factual misunderstanding
- missing explanation
- missing experiment
- methodological concern
- writing clarity
- scope disagreement
- valid limitation

对于每条评论：
1. 复述 reviewer 真正担心什么
2. 判断是否成立
3. 给出直接回答
4. 必要时提供新证据 / 新实验
5. 明确论文会如何修改

Rebuttal 语气要专业、直接、可验证。
不要使用“reviewer clearly misunderstood”一类对抗性表达。
不要用大量感谢套话挤占字数。
```

---

# 23. 中文正式写作 Prompt

```text
使用现代、自然、正式的中文书面语。

避免：
- 过度使用“赋能、助力、打造、推动、深入、全面、持续、有效”等泛化动词
- 每段都使用“首先、其次、再次、最后”
- 大量四字词堆砌
- 为了正式而把简单句改成行政公文腔
- 频繁使用“值得注意的是”“不难发现”“显而易见”
- 句尾连续出现“具有重要意义”“提供有力支撑”

优先：
- 明确主语
- 具体动作
- 清晰因果
- 准确术语
- 自然段落

专业文章允许长句，但长句内部必须存在清楚的逻辑层次。
```

---

# 24. 中英双语写作 Prompt

```text
生成中英双语版本时，不要逐字翻译。

保持两种语言中的：
- 事实一致
- 论点一致
- 技术术语一致
- 信息密度大致一致

中文应符合中文书面表达习惯。
英文应符合英语自然语序与语域。

不要让英文保留中文句法，也不要让中文成为英语结构的机械映射。

专有名词、论文名、模型名和正式技术术语应保持标准写法。
```

---

# 25. 极简压缩 Prompt

```text
把文本压缩到原长度的 [50% / 30% / 指定字数]。

优先删除：
- 重复观点
- 元话语
- 空洞修饰
- 可以从上下文推断出的解释
- 重复总结

优先保留：
- 核心结论
- 关键事实
- 因果关系
- 条件与限制
- 必要数字
- 专业术语

不要通过删除逻辑前提来换取字数。
```

---

# 26. 扩写 Prompt

```text
扩写下面内容，但不要通过同义改写和增加空话来扩充字数。

每增加一段，都必须至少增加一种东西：
- 新解释
- 新机制
- 新证据
- 新例子
- 新边界条件
- 新比较
- 新推论

如果没有新的信息可以增加，就不要继续扩写。
```

---

# 27. “先结构，后正文” Prompt

适合篇幅较长、逻辑复杂的任务。

```text
不要立即写正文。

先输出一个内容架构，要求每一节都回答：
- 这一节解决什么问题
- 依赖前文什么知识
- 引入什么新知识
- 与下一节如何连接

检查是否存在：
- 顺序倒置
- 前置概念未定义
- 重复章节
- 章节功能重叠
- 没有推进主线的内容

修正结构后，再按这个架构写正文。
```

---

# 28. “反模板”检查表

可以追加到任意 Prompt 末尾。

```text
最终检查并删除以下模式，除非上下文确实需要：

- In today's rapidly evolving world...
- It is important to note that...
- It is worth noting that...
- Let's delve into...
- This is not just X; it is Y.
- The question is... The answer is...
- At its core...
- In conclusion...
- Overall...
- Ultimately...
- game-changing
- transformative
- revolutionary
- unlock
- leverage（当普通 use 更准确时）
- foster（当具体动词更准确时）

不要机械替换这些词。
真正目标是删除没有信息价值的表达。
```

---

# 29. 推荐工作流

长文本建议：

```text
1. Task specification
2. Source collection
3. Argument / concept map
4. Outline
5. First draft
6. Structural edit
7. Sentence-level edit
8. Fact / citation check
9. Style consistency check
10. Final output
```

不要把所有工作压进一个超长 Prompt。复杂任务拆成独立 pass，通常比一次性塞入几十条约束更稳定。

---

# 30. 来源与进一步阅读

以下来源用于整理本文档的主要思想。社区来源仅作为实践参考，不表示其中所有建议都被采纳。

## OpenAI / 官方

- OpenAI Developers — latest model guidance / GPT-6 Astra  
  https://developers.openai.com/api/docs/guides/latest-model?model=gpt-6-astra

- OpenAI Academy — Writing with ChatGPT  
  https://openai.com/academy/writing/

- OpenAI Academy — Customizing ChatGPT / writing style workflows  
  https://academy.openai.com/public/clubs/work-users-ynjqu/resources/customizing-chatgpt

- OpenAI Academy — Improve your papers without losing your voice  
  https://academy.openai.com/public/clubs/higher-education-05x4z/blogs/improve-your-papers-without-losing-your-voice-2026-05-18

- OpenAI Academy — Draft and revise academic documents in ChatGPT  
  https://academy.openai.com/en/public/clubs/higher-education-05x4z/blogs/draft-and-revise-academic-documents-in-chatgpt-2026-05-19

## GitHub Prompt repositories

- Awesome ChatGPT Prompts  
  https://github.com/solo-yolo/awesome-chatgpt-prompts

- QAInsights / Awesome ChatGPT Prompts  
  https://github.com/QAInsights/awesome-chatgpt-prompts

- Awesome ChatGPT 中文资源  
  https://github.com/ai919/Awesome-ChatGPT

- GPT-6 Prompt Writer  
  https://github.com/gnipbao/gpt6-prompt-writer

## Community / discussion

- OpenAI Developer Community — writing style discussions  
  https://community.openai.com/

- Reddit — r/ChatGPTPromptGenius  
  https://www.reddit.com/r/ChatGPTPromptGenius/

- Reddit — r/PromptEngineering  
  https://www.reddit.com/r/PromptEngineering/

## 其他近期 GPT-6 Prompt 资料

- iWeaver GPT-6 Astra prompt examples  
  https://www.iweaver.ai/zh/blog/best-gpt-6-astra-prompts/

- Parth Skills GPT-6 Astra prompting guide  
  https://parthskills.com/blog/gpt-6-astra-prompting-guide/

---

# 31. 维护原则

后续新增 Prompt 时优先判断：

1. 它解决的具体失败模式是什么？
2. 约束是否可观察？
3. 能否通过输出判断 Prompt 是否生效？
4. 是否与已有规则重复？
5. 是模型通用规则，还是某一文体专项规则？
6. 是否只是在增加“世界级、顶尖、专业、深入”等无验证价值的形容词？

只有能回答这些问题的 Prompt，才值得长期保留。
