# Learning records

Store a JSON array in `~/.local/share/learn-english-with-ai/review.json`. Each saved correction is one object with exactly the fields below; conversational feedback and save prompts stay outside the record.

```json
[
  {
    "original": "maybe we could 结构化 these things for the later analysis",
    "non_english": "结构化",
    "english": "Maybe we could structure these learning records for later analysis.",
    "context": "Discussing how to store English-learning notes for later analysis.",
    "meaning": "Here, 结构化 means organizing learning records into consistent fields for analysis, not just formatting the text neatly.",
    "created": "2026-10-13"
  }
]
```

- `original`: the user's exact wording being corrected.
- `non_english`: the word or phrase from another language used in the original wording; `null` for English-only corrections.
- `english`: the suggested natural wording for this context.
- `context`: a short description of the situation.
- `meaning`: a brief explanation of the intended sense or tone and how the English conveys it, rather than just a dictionary definition.
- `created`: the date the item was saved, in `YYYY-MM-DD` format; the date above is an example.

Read existing records before saving. Add the approved item without replacing unrelated entries; update a recurring item only when its meaning and context match, preserving its creation date. Use separate items for different senses of the same expression. Create the file only after the user chooses **Save**.
