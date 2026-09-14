# Writing Prompts

写作类 Prompt 按用途分类维护。不要再把不同任务堆在一个超长文件里。

## Directory map

```text
writing/
├── 00-core/          # 所有写作任务共用的基础规则与任务规格
├── 01-style/         # 自然写作、风格控制、Style Profile
├── 02-long-form/     # 教科书、专著、长文、博客文章
├── 03-academic/      # 学术写作、Academic English、论文各章节
├── 04-technical/     # 技术写作、机制解释、数据流与数学表达
├── 05-professional/  # 邮件、商业与专业沟通
├── 06-creative/      # 小说、叙事与创意写作
├── 07-editing/       # 诊断、改写、自我编辑、事实与引用检查
└── 90-research/      # 来源、模型差异、反模式与 Prompt 研究笔记
```

## 推荐使用顺序

1. 先挂载 [`00-core/system-prompt.md`](00-core/system-prompt.md) 作为长期写作规则。
2. 用 [`00-core/task-specification.md`](00-core/task-specification.md) 描述当前任务。
3. 根据任务进入对应目录叠加专项 Prompt。
4. 初稿完成后使用 `07-editing/` 中的独立 revision / fact-check Prompt。

对于重要长文，推荐：

```text
Task specification
→ Outline / concept map
→ Draft
→ Structural revision
→ Sentence-level revision
→ Fact & citation check
→ Finalize
```
