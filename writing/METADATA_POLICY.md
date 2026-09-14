# Prompt Metadata Policy

所有 Prompt 文件统一采用以下结构：

````markdown
# Prompt title

<details>
<summary>Source & freshness</summary>

- Source: ...
- Status: official-derived / community-derived / repository-synthesis
- Last verified: YYYY-MM-DD
- Last updated: YYYY-MM-DD
- Full references: ...

</details>

```text
PROMPT BODY ONLY
```
````

## 规则

1. 来源、日期、验证状态永远放在 Prompt 代码块之外。
2. 可直接使用的 Prompt 必须完整放进 fenced code block，方便使用 GitHub 的 **Copy** 按钮。
3. 点击 Prompt 代码块右上角的 Copy 时，复制结果只能包含 Prompt 本体；不得包含来源、URL、版本日期、维护说明或 attribution。
4. 不在 Prompt 本体中插入引用、URL、脚注、版本日期或维护说明。
5. `Last verified` 表示最后一次核对主要来源、模型行为或相关官方材料的日期。
6. `Last updated` 表示该 Prompt 文件内容最后修改的日期。
7. `official-derived`：主要原则可以追溯到 OpenAI 官方 / first-party 材料，但仓库文本通常经过归纳、翻译或重组，不表示官方逐字 Prompt。
8. `community-derived`：主要来自公开社区实践并经筛选。
9. `repository-synthesis`：仓库根据多个来源、写作方法与具体使用场景综合形成。
10. 更完整的来源列表统一维护在 `90-research/sources.md`；专项文件只保留简短来源标签，避免影响复制体验。

## 日期语义

`Last verified` 和 `Last updated` 不应混用。例如，一个 Prompt 可能半年没有改动，但刚刚重新核验过 GPT-6 官方 guidance：此时只更新 `Last verified`，不必伪造新的内容更新时间。

如果模型版本、官方 prompting guidance 或明显相关的模型行为发生变化，应优先重新验证受影响文件，并更新 `Last verified`。
