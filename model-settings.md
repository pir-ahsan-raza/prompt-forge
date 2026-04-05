# Model Settings - What They Actually Do

These are the settings that matter and what changing them actually feels like
in practice. Not the documentation definition - the real-world effect.

---

## Temperature

Controls randomness. But "randomness" is a bad way to think about it.

Better mental model: **how willing the model is to pick a less obvious word.**

| Value | Feel |
|-------|------|
| 0.0 | Robotic. Same output every time. Good for structured data extraction. |
| 0.3–0.5 | Focused. Best for coding, analysis, anything where correctness matters. |
| 0.7–0.9 | Natural. Good for writing, brainstorming, conversation. |
| 1.0+ | Unpredictable. Sometimes brilliant, often useless. |

Default on most platforms is 0.7–1.0. For dev work, drop it to 0.3.

---

## Top-P (Nucleus Sampling)

Works with temperature. Limits which tokens the model even considers before
picking one.

Honest take: most people don't need to touch this. If your temperature is
set right, top-p tuning gives you marginal gains. Leave it at 0.9–1.0 unless
you're doing something specific.

---

## Max Tokens

Hard limit on output length. The model doesn't "try harder" to be concise -
it just stops. If a response gets cut off mid-sentence, this is why.

Set it high for long-form tasks. For short Q&A or classification, keep it low
so you're not burning tokens on padding.

---

## System Prompt

Most impactful setting that isn't a number. Sets the frame for the entire
conversation. A good system prompt does more than a high temperature ever will.

Worth spending time on. The prompts in this repo are a start.

---

## Frequency / Presence Penalty (OpenAI specific)

- **Frequency penalty**: Discourages the model from repeating the same word/phrase
- **Presence penalty**: Encourages the model to bring in new topics

Both default to 0. For long documents where the model tends to loop back on
itself, frequency penalty at 0.3–0.5 helps.

---

## My defaults

| Task | Temp | Top-P | Max Tokens |
|------|------|-------|------------|
| Coding | 0.2 | 0.9 | 2048 |
| Writing | 0.8 | 0.95 | 4096 |
| Brainstorming | 1.0 | 1.0 | 1024 |
| Data extraction | 0.0 | 1.0 | 512 |
