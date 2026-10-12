# Learn English with AI

A portable English-learning agent skill: improve your English while using AI for coding, writing, and everyday work. Includes brief corrections, contextual phrasing from other languages into English, formal and academic writing guidance, and spaced review. The behavior lives in [SKILL.md](SKILL.md).

Install this directory as `learn-english-with-ai` under each agent's supported user-level skills directory, then load or invoke it for ongoing coaching. Activation depends on the agent; one installation does not enable every agent automatically.

Each save prompt shows your original wording alongside its suggested replacement. Choose **Save** or **Don’t save** for each correction, one at a time, through the agent’s interactive choice tool (`ask` in OMP), or in text if unavailable. Learning items are recorded only with your explicit approval. Records live outside this repository at `~/.local/share/learn-english-with-ai/review.json`. The [structured format](references/learning-records.md) keeps non-English expressions, English suggestions, context, meaning, and creation dates available for later analysis. Recording needs filesystem access. Reviews happen during conversations, not as background notifications.

Review combines [spaced practice and active retrieval](https://learninglab.psych.purdue.edu/downloads/2011/inpress_Roediger_Karpicke_Bjorkfest_Chapter.pdf).
