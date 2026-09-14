# Sources

本仓库优先从官方、近期、可验证资料提炼写作 Prompt；社区 Prompt 主要用于发现实践模式和失败模式，不无条件照搬。

## OpenAI official / first-party

### GPT-6 Astra Model Guidance

https://developers.openai.com/api/docs/guides/latest-model

重点：GPT-6 Astra 的 prompting best practices，尤其是 Personality and writing style。官方明确建议：当应用需要较少格式化的 prose 时，应显式要求清晰自然段、只在信息真正并列/顺序/比较时使用列表、使用 familiar words / concrete examples / precise verbs / active voice / direct statements，并指出 Astra 容易出现较多列表、表格、Markdown 与跨回答重复措辞。

### Writing with ChatGPT — OpenAI Academy

https://openai.com/academy/writing/

重点：Plan → Draft → Revise → Package；明确 goal、audience、ask、raw material、constraints 和 output format；长文本先做结构/outline；有针对性的 revision pass 通常优于反复要求“make it better”。

### Draft and Revise Academic Documents in ChatGPT

https://academy.openai.com/en/public/clubs/higher-education-05x4z/blogs/draft-and-revise-academic-documents-in-chatgpt-2026-05-19

重点：学术文档适合做 narrow、inspectable 的 transformation / revision；应保留原意，明确哪些内容仍需人工事实核验、引用核验和专业判断。

### Improve Your Papers Without Losing Your Voice

https://academy.openai.com/public/clubs/higher-education-05x4z/blogs/improve-your-papers-without-losing-your-voice-2026-05-18

重点：使用 ChatGPT 改善 clarity、structure、flow 时保留作者自己的观点与 voice。

## Community / prompt repositories

社区来源后续按以下优先级继续扩充：

1. OpenAI Developer Community 中可复现的写作实践
2. GitHub 大型 Prompt repositories
3. Reddit r/PromptEngineering / r/ChatGPTPromptGenius 等社区的高质量讨论
4. 针对 GPT-6 的近期实测文章或 Prompt collections

社区资料进入主库前需要：去重、去 detector-optimization、去虚构资历依赖，并改写成可观察的写作约束。

## Citation / attribution policy

- 官方原始 Prompt 若需要逐字保存，应注明来源并控制引用长度。
- 大多数社区 Prompt 以“思想提炼 + 重写”的方式收录，而不是大段复制。
- 对模型行为的时效性结论需要记录日期和对应模型。
- 模型升级后，旧 Prompt 不自动视为最佳实践，应重新验证。

> Last reviewed: 2026-09-14
