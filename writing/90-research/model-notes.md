# Model-specific Writing Notes

## GPT-6 Astra

As of 2026-09-14, prioritize explicit style and structure constraints.

Observed / documented tendencies worth controlling:
- tends to use detailed formatting, lists, tables, and Markdown when not constrained
- may reuse recurring phrases across sessions
- responds well to explicit prose preferences
- stronger instruction following makes detailed style rules more useful, but contradictory rules also matter more
- for long tasks, task boundaries and definition of done should be explicit

Recommended baseline:
- clear paragraphs, one main idea per paragraph
- lists only for genuinely parallel/sequential/comparative information
- familiar words, concrete examples, precise verbs
- active voice and direct statements
- main point early
- enough supporting detail to be useful
- explicit anti-patterns only where recurring failure is observed

Primary source:
https://developers.openai.com/api/docs/guides/latest-model

## GPT-5.6 Sol

Most task-specification, grounding, structure, revision, and anti-template prompts in this repository remain applicable. Model-specific behavior should not be assumed identical to GPT-6 Astra; test important production prompts separately.

## Maintenance rule

Do not create a new folder for every model unless the behavior difference changes prompting strategy materially. Prefer stable task-oriented prompts plus a small model-notes layer.
