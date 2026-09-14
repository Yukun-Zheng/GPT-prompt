# GPT Prompt Library

一个面向现代 GPT 的结构化 Prompt 仓库。当前优先维护 **GPT-6 Astra / GPT-5.6** 的高质量写作 Prompt，后续可继续扩展 research、coding、agents 等任务族。

> Last updated: 2026-09-14

## Repository structure

```text
GPT-prompt/
├── README.md
└── writing/
    ├── README.md
    ├── METADATA_POLICY.md
    ├── 00-core/
    │   ├── system-prompt.md
    │   └── task-specification.md
    ├── 01-style/
    │   ├── natural-prose.md
    │   ├── style-profile.md
    │   └── chinese-formal.md
    ├── 02-long-form/
    │   ├── textbook-monograph.md
    │   └── article-blog.md
    ├── 03-academic/
    │   ├── general-academic.md
    │   ├── academic-english.md
    │   ├── literature-review.md
    │   └── paper/
    │       ├── abstract.md
    │       ├── introduction.md
    │       ├── related-work.md
    │       ├── method.md
    │       ├── experiments.md
    │       └── rebuttal.md
    ├── 04-technical/
    │   └── technical-writing.md
    ├── 05-professional/
    │   ├── email.md
    │   └── marketing-copy.md
    ├── 06-creative/
    │   └── fiction-storytelling.md
    ├── 07-editing/
    │   ├── diagnostic-edit.md
    │   ├── self-revision.md
    │   └── fact-citation-check.md
    └── 90-research/
        ├── sources.md
        ├── model-notes.md
        └── anti-patterns.md
```

## 分类逻辑

目录按“Prompt 要解决什么问题”划分，而不是按某次聊天或某个来源堆文件：

- **00-core**：任何写作任务都可以叠加的基础层。
- **01-style**：只控制语言、节奏、作者风格与中文表达。
- **02-long-form**：解决跨章节、长程一致性和知识组织。
- **03-academic**：论文、survey、Academic English；`paper/` 再细到论文具体章节。
- **04-technical**：机制、系统、算法、公式、shape 和数据流表达。
- **05-professional**：邮件、商业文案等专业沟通。
- **06-creative**：小说、故事和连续叙事。
- **07-editing**：与生成初稿分离的诊断、revision、事实/引用核验。
- **90-research**：Prompt 来源、模型行为差异、反模式研究；不作为日常直接调用入口。

## Source & freshness，不妨碍复制

每个可直接使用的 Prompt 文件可以标注：

- `Source`：主要来源或综合依据
- `Status`：`official-derived` / `community-derived` / `repository-synthesis`
- `Last verified`：最后一次重新核验来源、模型 guidance 或相关行为的日期
- `Last updated`：Prompt 内容最后修改日期

这些信息全部放在 Prompt 代码块之外，并优先折叠在 `<details>` 中。**Prompt 本体始终完整放在 fenced code block 内。**

因此在 GitHub 上点击代码块右上角 **Copy** 时，复制到的只有 Prompt，不会带上引用、URL、日期或维护说明。

详细规范见 [`writing/METADATA_POLICY.md`](writing/METADATA_POLICY.md)，完整来源账本见 [`writing/90-research/sources.md`](writing/90-research/sources.md)。

## 最推荐的组合方式

不要寻找一个不断膨胀的“万能 Prompt”。推荐按层组合：

```text
00-core/system-prompt.md
+ 00-core/task-specification.md
+ 一个任务专项 Prompt
+ 必要的 style Prompt
+ 独立 editing / fact-check pass
```

例如写一篇机器人论文 Method：

```text
00-core/system-prompt.md
+ 00-core/task-specification.md
+ 03-academic/paper/method.md
+ 04-technical/technical-writing.md
+ 07-editing/fact-citation-check.md
```

写一本技术教材章节：

```text
00-core/system-prompt.md
+ 02-long-form/textbook-monograph.md
+ 04-technical/technical-writing.md
+ 01-style/chinese-formal.md
+ 07-editing/self-revision.md
```

## 核心原则

相比旧式：

```text
You are a world-class award-winning writer with 30 years of experience...
```

更推荐控制可观察变量：

```text
目标
→ 受众
→ 材料与事实边界
→ 结构
→ 风格
→ 禁止项
→ 验收标准
→ 独立修订与核验
```

现代 GPT 已经不太需要靠虚构资历“进入角色”。更稳定的方法是把任务定义、信息边界、文本结构和完成标准写清楚。

## 来源优先级

1. OpenAI 官方模型 / prompting / writing guidance
2. OpenAI Academy
3. OpenAI Developer Community
4. GitHub 高质量 Prompt repositories
5. Reddit / PromptEngineering 社区中的高质量实践
6. 近期针对 GPT-6 的实测资料

详见 [`writing/90-research/sources.md`](writing/90-research/sources.md)。

## Maintenance

新 Prompt 进入仓库时先判断它属于哪一种“能力层”，不要默认继续往根目录加文件。

如果一个新 Prompt 同时涉及多个目录，优先拆成可组合模块，而不是复制多份。模型专属差异统一记录到 `90-research/model-notes.md`，只有差异足够大时才建立新的 model-specific 子目录。
