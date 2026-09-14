# Sources

本仓库优先从官方、近期、可验证资料提炼写作 Prompt；社区 Prompt 主要用于发现实践模式和失败模式，不无条件照搬。

> Last reviewed: 2026-09-14

## OpenAI official / first-party

### GPT-6 Astra Model Guidance

https://developers.openai.com/api/docs/guides/latest-model

Checked: 2026-09-14

重点：GPT-6 Astra 的 prompting best practices，尤其是 Personality and writing style。官方明确建议：当应用需要较少格式化的 prose 时，应显式要求清晰自然段、只在信息真正并列/顺序/比较时使用列表、使用 familiar words / concrete examples / precise verbs / active voice / direct statements，并指出 Astra 容易出现较多列表、表格、Markdown 与跨回答重复措辞。

主要支持：`00-core/system-prompt.md`、`01-style/natural-prose.md`、`01-style/chinese-formal.md`、`04-technical/technical-writing.md`、`05-professional/marketing-copy.md`。

### GPT-6 Astra Model Page

https://developers.openai.com/api/docs/models/gpt-6-astra

Checked: 2026-09-14

用途：核验当前模型名称、能力定位和模型级状态；不把模型规格页本身当成写作 Prompt 来源。

### Writing with ChatGPT — OpenAI Academy

https://openai.com/academy/writing/

Published: 2026-04-10  
Checked: 2026-09-14

重点：`Plan → Draft → Revise → Package`；明确 goal、audience、ask、raw material、constraints 和 output format；长文本先做结构/outline；有针对性的 revision pass 通常优于反复要求“make it better”；涉及数字、政策或具体 claim 时应验证事实。

主要支持：`00-core/task-specification.md`、`02-long-form/*`、`05-professional/email.md`、`07-editing/*`。

### Customizing ChatGPT — OpenAI Academy

https://academy.openai.com/public/clubs/work-users-ynjqu/resources/customizing-chatgpt

Published: 2025-09-25  
Last updated by source: 2026-05-29  
Checked: 2026-09-14

重点：可提供自己的写作样本，让 ChatGPT 总结 tone/style（包括 word choice、sentence length、formality 等），再要求在新文本中 mirror tone、pacing、structure。

主要支持：`01-style/style-profile.md`。

### Draft and Revise Academic Documents in ChatGPT

https://academy.openai.com/en/public/clubs/higher-education-05x4z/blogs/draft-and-revise-academic-documents-in-chatgpt-2026-05-19

Published: 2026-05-20  
Checked: 2026-09-14

重点：学术文档适合做 narrow、inspectable 的 transformation / revision；应保留原意，明确哪些内容仍需人工事实核验、引用核验和专业判断。

主要支持：`03-academic/*`、`03-academic/paper/*`、`07-editing/fact-citation-check.md`。

### Improve Your Papers Without Losing Your Voice

https://academy.openai.com/public/clubs/higher-education-05x4z/blogs/improve-your-papers-without-losing-your-voice-2026-05-18

Published: 2026-05-18  
Checked: 2026-09-14

重点：使用 ChatGPT 改善 clarity、structure、flow 时保留作者自己的观点与 voice；比较 minimal edit 与 stronger revision，并解释修改原因；不要引入作者未提出的新 claim。

主要支持：`03-academic/general-academic.md`、`07-editing/diagnostic-edit.md`、`07-editing/self-revision.md`。

## OpenAI Developer Community

### Story writing — change in writing style

https://community.openai.com/t/story-writing-change-in-writing-style/1115400/3

Original discussion: 2025-02  
Checked: 2026-09-14

重点：社区用户针对 creative writing 总结了 fluid / immersive prose、避免 excessive fragmentation、避免 forced dramatization、通过 subtlety 建立 psychological tension、保持 consistent pacing 和 character-driven storytelling 等可观察约束。

说明：这是社区经验，不代表 OpenAI 官方建议。仓库只提炼其可复现的写作控制思想，不逐字保存原 Prompt。

主要支持：`06-creative/fiction-storytelling.md`。

## Community / prompt repositories

社区来源后续按以下优先级继续扩充：

1. OpenAI Developer Community 中可复现的写作实践
2. GitHub 大型 Prompt repositories
3. Reddit r/PromptEngineering / r/ChatGPTPromptGenius 等社区的高质量讨论
4. 针对 GPT-6 的近期实测文章或 Prompt collections

社区资料进入主库前需要：去重、去 detector-optimization、去虚构资历依赖，并改写成可观察的写作约束。

## Source status labels

Prompt 文件中的 `Status` 使用以下标签：

- `official-derived`：主要原则可以追溯到 OpenAI 官方 / first-party 材料，但仓库版本通常经过归纳、翻译或重组，不表示官方逐字 Prompt。
- `community-derived`：包含公开社区中出现并经过筛选的实践模式。
- `repository-synthesis`：由本仓库基于多个来源、写作方法和具体使用场景综合形成。

一个文件可以同时拥有多个标签。

## Freshness fields

- `Last verified`：最后一次重新核对主要来源、模型行为或相关官方材料的日期。
- `Last updated`：该 Prompt 文件内容最后修改的日期。
- `Published / Last updated by source`：仅在原网页明确提供时记录来源自身的发布日期或更新日期。

`Last verified` 不等于“Prompt 在此日期由 OpenAI 官方发布”。它只表示仓库维护者在该日期重新核验过相关依据。

## Citation / attribution policy

- 官方原始 Prompt 若需要逐字保存，应注明来源并控制引用长度。
- 大多数社区 Prompt 以“思想提炼 + 重写”的方式收录，而不是大段复制。
- 对模型行为的时效性结论需要记录日期和对应模型。
- 模型升级后，旧 Prompt 不自动视为最佳实践，应重新验证。
- 来源、日期、URL 和维护说明不得插入可直接复制的 Prompt code block。

## Copyability policy

所有可直接使用的 Prompt 都应完整放在 fenced code block 中。来源和 freshness 元数据放在代码块外，并优先折叠在 `<details>` 中。这样在 GitHub 使用代码块 Copy 按钮时，只会复制 Prompt 本体。

具体规范见 [`../METADATA_POLICY.md`](../METADATA_POLICY.md)。
