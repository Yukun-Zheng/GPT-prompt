# Writing Prompts / 写作提示词

写作类 Prompt 按用途分类维护。不要再把不同任务堆在一个超长文件里。

## Directory map / 目录

```text
writing-写作/
├── README.md
├── METADATA_POLICY.md              # 来源、日期、双语与可复制性规范
├── 00-core-核心/                   # 所有写作任务共用的基础规则与任务规格
├── 01-style-风格/                  # 自然写作、风格控制、Style Profile
├── 02-long-form-长文/              # 教科书、专著、长文、博客文章
├── 03-academic-学术/               # 学术写作、Academic English、论文各章节
│   └── paper-论文各部分/           # Abstract / Introduction / Method / Experiments 等
├── 04-technical-技术写作/          # 机制解释、数据流与数学表达
├── 05-professional-专业沟通/       # 邮件、商业与专业沟通
├── 06-creative-创意写作/           # 小说、叙事与创意写作
├── 07-editing-编辑校对/            # 诊断、改写、自我编辑、事实与引用检查
└── 90-research-来源研究/           # 来源、模型差异、反模式与 Prompt 研究笔记
```

目录名统一使用 `English-中文`：英文保证路径语义稳定、方便搜索；中文让目录用途可以直接读懂。

## 直接复制

每个可直接使用的 Prompt 都完整放在 fenced code block 中。来源、验证日期和维护状态放在代码块外的折叠区域：

- `Source`：主要依据
- `Status`：`official-derived` / `community-derived` / `repository-synthesis`
- `Last verified`：最后重新核验来源或模型行为的日期
- `Last updated`：Prompt 内容最后修改日期

因此在 GitHub 上直接点击 Prompt 代码块右上角 **Copy**，复制到的只有 Prompt 本体，不会带上来源、URL 或日期。

### 中文 / English

仓库默认优先保证**中文版可直接使用**。

如果一个 Prompt 同时保留中文和英文版本：

- `## 中文版（直接复制）` 下只放一个纯中文 Prompt 代码块
- `## English version (copy directly)` 下只放一个纯英文 Prompt 代码块
- 两种语言不放在同一个代码块里
- 来源、日期、翻译说明和维护信息全部留在代码块外

因此复制中文版时不会夹带英文，复制英文版时也不会夹带中文或任何元数据。

完整规范见 [`METADATA_POLICY.md`](METADATA_POLICY.md)，完整来源账本见 [`90-research-来源研究/sources.md`](90-research-来源研究/sources.md)。

## 推荐使用顺序

1. 先挂载 [`00-core-核心/system-prompt.md`](00-core-核心/system-prompt.md) 作为长期写作规则。
2. 用 [`00-core-核心/task-specification.md`](00-core-核心/task-specification.md) 描述当前任务。
3. 根据任务进入对应目录叠加专项 Prompt。
4. 初稿完成后使用 `07-editing-编辑校对/` 中的独立 revision / fact-check Prompt。

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
