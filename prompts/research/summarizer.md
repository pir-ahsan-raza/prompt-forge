# Research Summarizer - Cut Through the Noise

**Use when:** You've got a wall of text (article, paper, docs page, thread) and you need the actual substance fast. Also useful for comparing multiple sources without reading all of them.

---

## The Prompt

```
Summarize this for me. I'm a developer with [X years] experience, so don't dumb it down — I just don't have time to read the full thing.

Give me:
1. The main point in one sentence
2. The 3-5 things that actually matter (not a full outline — the stuff I'd regret not knowing)
3. Anything that's counterintuitive or contradicts common assumptions
4. What I'd need to do differently based on this (if anything)

Skip the background context and methodology unless it directly changes how I should interpret the results.

Source:
[PASTE TEXT]
```

---

## Variations

**Comparing two approaches/tools/libraries:**
```
I'm deciding between [A] and [B]. Don't give me a balanced "both have their uses" answer. Based on what I tell you about my situation, give me a direct recommendation and explain the one or two things that tipped it.

My situation: [describe your use case, team size, constraints]

[PASTE OR DESCRIBE BOTH OPTIONS]
```

**For long documentation pages:**
```
I need to [accomplish specific task] using [tool/library]. Pull only what's relevant to that from this doc. Ignore everything else.

Task: [what you're trying to do]
Docs:
[PASTE]
```

**For academic papers / research:**
```
What did they actually find? Skip the abstract, intro, and discussion. Just the findings, the sample size, and whether there's a reason to be skeptical of the methodology.

Paper:
[PASTE]
```

---

## Notes

The "3-5 things that matter" framing works much better than "summarize in bullet points" - the latter gives you an outline, the former gives you judgment. There's a difference.

If the source is very long, paste it in chunks and use: "Keep a running summary. Don't finalize yet." Then on the last chunk: "Now give me the full summary."
