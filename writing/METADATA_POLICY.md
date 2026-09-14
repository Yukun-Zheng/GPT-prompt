# Prompt Metadata Policy

所有 Prompt 文件统一采用以下结构：

```markdown
# Prompt title

<details>
<summary>Source & freshness</summary>

- Source: ...
- Last verified: YYYY-MM-DD
- Last updated: YYYY-MM-DD
- Status: official-derived / community-derived / repository-synthesis

</details>

```text
PROMPT BODY ONLY
```
```

## 规则

1. 来源、日期、验证状态永远放在 Prompt 代码块之外。
2. 可直接使用的 Prompt 必须完整放进单个 fenced code block，方便使用 GitHub 的 Copy 按钮。
3. 不在 Prompt 本体中插入引用、URL、脚注、版本日期或维护说明。
4. `Last verified` 表示最后一次核对主要来源或模型行为的日期；`Last updated` 表示文件内容最后修改日期。
5. `official-derived`：主要来自 OpenAI 官方材料并经整理；`community-derived`：主要来自公开社区实践并经筛选；`repository-synthesis`：仓库根据多个来源和写作原则综合形成。
6. 更完整的来源列表统一维护在 `90-research/sources.md`，专项文件只保留简短来源标签，避免影响复制体验。
