# Humanize Writing Tone

**Use when:** You've drafted something (or AI drafted it for you) and it reads stiff, generic, or weirdly formal. Good for blog posts, READMEs, LinkedIn posts, internal docs, emails.

---

## The Prompt

```
Rewrite the following text so it sounds like a real person wrote it — someone who's thoughtful but not trying to impress anyone. Keep the meaning identical. Don't add fluff, don't remove detail.

Specific things to fix:
- Replace passive voice with active where it doesn't sound forced
- Break up any sentence over 25 words that doesn't need to be that long
- Remove phrases like "it's worth noting", "in today's world", "leverage", "utilize", "delve", "dive in", "let's explore", "it's important to", "seamlessly"
- If a paragraph starts with "In conclusion" or "To summarize" — cut that opener, just say the thing
- Keep contractions where they fit naturally (don't force them)
- If there's a list of 3+ items that reads like bullet soup, see if it flows better as a sentence

Don't explain what you changed. Just return the rewritten version.

Text:
[PASTE YOUR TEXT HERE]
```

---

## Variations

**For technical writing (docs, READMEs):**
Add this line after the main instruction:
> Keep all technical terms exactly as-is. Only rewrite the surrounding prose.

**For short-form (tweets, captions, one-liners):**
> Same rules, but also cut word count by 30% without losing the point.

**For emails:**
> Tone should be direct and warm - like a colleague you actually like, not a press release.

---

## Notes

Works best when you give it full paragraphs, not bullet points. If you paste bullets, it'll just clean up each bullet, which is fine, but you lose the flow improvements.

The phrase blacklist above is the most important part. Models love those filler phrases and will sneak them back in on revision. If you're running multiple passes, re-include the blacklist each time.
