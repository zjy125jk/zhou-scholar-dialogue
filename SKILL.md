---
name: zhou-scholar-dialogue
description: Rewrite modern Chinese, plain-language, or lightly literary questions into era-consistent Zhou or broadly pre-Qin scholarly discourse. Use when the user wants to consult an ancient Chinese learned figure without revealing modern identity, maintain a persona of a humble but well-read junior, translate modern abstractions into period-safe categories, produce safe follow-up lines, or generate a reusable prompt for this masquerade workflow.
---

# Zhou Scholar Dialogue

## Overview

Use this skill to package a user's real question for a Zhou-era or broadly pre-Qin scholar. Hide modernity first; elegance is secondary.

Preserve a speaker who sounds like a respectful junior with real book-learning, but not a reckless quote-machine. Prefer stable plausibility over ornate prose.

## Default to a Safe Persona

Default to:

- a broad Two-Zhou register
- a slight Spring and Autumn flavor
- a humble junior speaker
- moderate elegance, not full obscurity
- paraphrased classical learning instead of brittle exact quotation

Use speaker labels such as:

- `后学`
- `末学`
- `晚生`
- `不敏`
- `小子`

Use request phrases such as:

- `窃尝闻之`
- `未审其故`
- `敢请教`
- `愿闻其详`
- `窃有所惑`

Avoid:

- arrogance
- courtroom-style cross-examination
- obvious modern abstractions
- long fake quotations with made-up provenance

## Route the Period

Route the voice by period only when the user explicitly asks for it.

Use these defaults:

- `西周`: more formal, ritual-heavy, less dialectical
- `春秋`: courtly, consultative, morally framed, easiest default
- `战国`: sharper distinctions, stronger debate energy, still historically bounded

If the user does not specify a narrower setting, stay with a broad Zhou register that leans Spring and Autumn.

## Rewrite with This Workflow

### 1. Detect the task shape

Distinguish among:

- question packaging only
- question packaging plus follow-up lines
- full reusable prompt or system prompt for the masquerade workflow
- packaging plus direct answer, only if the user explicitly asks for both

Default to packaging only. Do not answer for the ancient scholar unless asked.

### 2. Remove modern leakage

Strip or rewrite:

- modern disciplines and abstractions
- post-Qin institutions unless the user explicitly sets a later period
- modern technologies, nation-state assumptions, and scientific framing
- analytical jargon that no Zhou scholar would use

Do not carry over words such as:

- `社会`
- `科学`
- `哲学`
- `逻辑`
- `系统`
- `理论`
- `结构`
- `经济`
- `政治`
- `心理学`
- `方法论`
- `效率`
- `数据`
- `信息`
- `意识形态`
- `民族国家`

Read [references/term-map.md](references/term-map.md) when the raw question contains modern abstractions or policy language.

### 3. Translate into pre-Qin categories

Reframe the issue in categories a Zhou or broadly pre-Qin scholar could accept, such as:

- `先王之道`
- `礼乐刑政`
- `名分伦序`
- `名实之辨`
- `德位`
- `教化风俗`
- `心志好恶`
- `治乱兴亡`
- `本末先后`
- `财用生民`

Prefer semantic translation over literal substitution. Convert the user's real concern into a period-safe line of inquiry.

Examples:

- "politics" -> `为政之道` or `邦国之治`
- "economy" -> `生民之计` or `财用之道`
- "social order" -> `上下之分` or `邦家之纪`
- "psychology" -> `心志` or `好恶之端`
- "institution design" -> `礼制` `官制` `成法`

### 4. Compose the voiced question

Write the question as if spoken by a respectful junior who has read some classics.

Do this:

- open with humility
- show learning through concepts, not through citation stunts
- keep the point sharp enough for discussion
- leave the elder room to teach

Prefer turns such as:

- `后学窃有所惑`
- `窃尝闻先王所以设礼者`
- `后学未达其故`
- `愿闻其详`

Prefer paraphrases such as:

- `按《诗》《书》之旨`
- `先王所以立礼者`
- `古人论治乱之故`

Do not fabricate exact quotations unless they are extremely short, stable, and necessary. When in doubt, paraphrase the idea instead of inventing wording.

### 5. Prepare safe continuations

Give 2 to 4 short follow-up lines that:

- keep the user in character
- buy time
- invite elaboration from the elder
- avoid forcing the user into exact chapter-and-verse recall

Use continuations such as:

- `后学非敢遽定其说，特欲闻其本末。`
- `此中轻重先后，愿更闻教。`
- `后学所疑者，正在其所由然耳。`

### 6. Emit short warnings

Point out:

- which words must not be said
- which direction of follow-up may expose modernity
- which safer semantic lane to stay in

Keep the warnings short and practical.

## Obey These Guardrails

- Never expose the user as a modern person.
- Never mention that the user has not read the classics.
- Never overperform by spraying names, chapter titles, and exact lines that may be wrong.
- Never smuggle in modern categories without translation.
- Never keep the raw premise if the premise itself is anachronistic.
- Never cite Han, Buddhist, Daoist religious, Song, Ming, Qing, or modern texts by default when the user only says "周朝" or "先秦".

If the user's real question cannot exist cleanly in Zhou terms, convert it into the nearest period-safe inquiry instead of forcing a literal rewrite.

## Use This Output Contract

Default to this structure unless the user explicitly asks for a different shape:

```text
【可直说版】
...

【更雅一点版】
...

【可续接的话】
1. ...
2. ...
3. ...

【避雷提醒】
- ...
- ...
- ...
```

Use `【可直说版】` for the practical version the user can send immediately.

Use `【更雅一点版】` for a slightly denser and more literary alternative.

Use `【可续接的话】` to preserve the persona under pressure.

Use `【避雷提醒】` to point out anachronisms, risky terms, and safe substitutions.

If the user asks only for a reusable prompt or system prompt, skip the block format and deliver the prompt directly.

## Read References Selectively

- Read [references/term-map.md](references/term-map.md) when the question contains modern political, social, economic, philosophical, or psychological wording.
- Read [references/examples.md](references/examples.md) when you need style targets or need to calibrate tone against realistic user inputs.
