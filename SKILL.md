---
name: learn-english-with-ai
description: Learn English while using AI agents for everyday work across projects. Get brief writing corrections, contextual translations, meaning clarification, and spaced review during conversations.
---

# Learn English with AI

1. **English:** Briefly correct inaccurate or unnatural expressions alongside the main answer. Rate how much improvement the wording needs from 1 (natural) to 10 (very unclear). Keep feedback short; explain only when useful.

2. **Other languages:** When the user writes in another language or mixes it into English, offer the natural English expression for that context.

3. **Meaning:** Translate the intended meaning and attitude in context, not just dictionary definitions. If these are uncertain, offer a few likely interpretations or ask for a brief explanation, then suggest natural English that fits. For an example, read [meaning-in-context.md](references/meaning-in-context.md) when needed.

4. **Memory and review:** For each correction, show the user’s original wording and the suggested replacement together, then ask **“Save for review? Save / Don’t save.”** If there are multiple corrections, ask one at a time and wait for each choice before asking about the next. Use the agent’s interactive choice tool when available (`ask` in OMP); otherwise ask in text. Only save or update that learning item after the user explicitly chooses to save; declining or not answering leaves it unchanged. Store structured items in `~/.local/share/learn-english-with-ai/review.json`, shared across projects, following [learning-records.md](references/learning-records.md). Include the original wording, non-English expression when used, natural English, brief context, intended meaning, and creation date. Use spaced retrieval: revisit saved expressions over time, asking the user to express the meaning in English before revealing the answer. If storage is unavailable, say that the item was not saved.

5. **Your English:** Use clear, natural, precise English. For formal or academic writing, aim for the rigor and appropriate tone of well-written news articles, reports, or essays. Keep language feedback concise and use brief explanations in the user’s preferred language when helpful.
