# ADR 0001: Why every sentence received a suggestion

- Date: 2026-11-02
- Status: Accepted

## Problem

The user reported that even simple English sentences triggered advice about punctuation and capitalization, followed by a save-for-review choice. The intended experience was an optional learning suggestion when an expression was genuinely unnatural.

## Likely cause

The earlier skill combined three instructions:

- “Briefly correct inaccurate or unnatural expressions alongside the main answer.”
- “Rate how much improvement the wording needs from 1 (natural) to 10 (very unclear).”
- “For each correction,” offer a save-for-review choice.

The rating instruction included natural wording in its scoring range. Together, these instructions plausibly encouraged evaluating every message, finding a small improvement, and offering to save it. The mixed-language instruction also broadly requested an English expression whenever another language appeared.

A smoke run with the earlier skill produced a punctuation correction, a 1/10 rating, and a save prompt for “thanks that works.” This demonstrated the reported behavior. The contribution of any individual word remains unverified.

## Decision in this commit

Revise [SKILL.md](../../SKILL.md) to make useful learning the criterion for offering feedback:

- Offer brief, optional corrections for genuinely unnatural English.
- Leave wording that is natural enough for its context alone.
- Remove the routine rating instruction.
- Handle cosmetic proofreading when requested.
- Offer English expressions for other languages when useful in context.

Preserve the existing meaning-clarification and review-storage behavior.

## Verification and tradeoff

Seven model-response smoke cases exercised the revised wording. Natural English and cosmetic-only messages received ordinary replies. Grammar and collocation errors and a translation gap received suggestions with review choices. Requested proofreading and ambiguous-meaning explanations also worked in the exercised cases.

The usefulness threshold requires contextual judgment, so feedback frequency may vary across models and conversations. The smoke runs covered response text; interactive tool behavior and record persistence were outside their scope.
