# Prompt Metadata Policy

所有 Prompt 文件统一采用“元数据在外、Prompt 本体在独立代码块内”的结构。

## 单语言文件

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

## 双语文件

如果 Prompt 同时提供中文和英文，两种语言必须使用**两个完全独立的代码块**：

````markdown
## 中文版（直接复制）

```text
中文 Prompt 本体
```

## English version (copy directly)

```text
English prompt body
```
````

语言标题、来源、日期、说明和链接一律留在代码块外。这样点击任一代码块右上角的 **Copy**，复制结果只包含该语言的 Prompt 本体。

## 规则

1. 来源、日期、验证状态永远放在 Prompt 代码块之外。
2. 可直接使用的 Prompt 必须完整放进单个 fenced code block，方便使用 GitHub 的 **Copy** 按钮。
3. 点击 Prompt 代码块右上角的 Copy 时，复制结果只能包含 Prompt 本体；不得包含来源、URL、版本日期、维护说明或 attribution。
4. 不在 Prompt 本体中插入引用、URL、脚注、版本日期或维护说明。
5. 若同一 Prompt 提供中英文版本，必须分别放入独立代码块，禁止在一个代码块中把两种语言拼接在一起。
6. 中文版应是可独立使用的 Prompt，不是夹杂“译文说明”的逐句注释版；必要的英文术语可以保留。
7. `Last verified` 表示最后一次核对主要来源、模型行为或相关官方材料的日期。
8. `Last updated` 表示该 Prompt 文件内容最后修改的日期。
9. `official-derived`：主要原则可以追溯到 OpenAI 官方 / first-party 材料，但仓库文本通常经过归纳、翻译或重组，不表示官方逐字 Prompt。
10. `community-derived`：主要来自公开社区实践并经筛选。
11. `repository-synthesis`：仓库根据多个来源、写作方法与具体使用场景综合形成。
12. 更完整的来源列表统一维护在 `90-research/sources.md`；专项文件只保留简短来源标签，避免影响复制体验。

## 日期语义

`Last verified` 和 `Last updated` 不应混用。例如，一个 Prompt 可能半年没有改动，但刚刚重新核验过 GPT-6 官方 guidance：此时只更新 `Last verified`，不必伪造新的内容更新时间。

如果模型版本、官方 prompting guidance 或明显相关的模型行为发生变化，应优先重新验证受影响文件，并更新 `Last verified`。
