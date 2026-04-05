# Write Docs That People Actually Read

**Use when:** You need to write documentation for a function, API, module, or project and you want it to be genuinely useful, not just technically complete.

---

## The Prompt

```
Write documentation for the following code. 

Rules:
- Lead with what it DOES and WHY someone would use it, not how it works internally
- Include a realistic usage example first, before parameter descriptions
- Note any gotchas, non-obvious behavior, or common mistakes in a "Watch out for" section
- If there are edge cases or error states, document them — don't pretend the happy path is the whole story
- Write like a developer who's been burned by bad docs before — include the things you'd wish you'd known

Don't document what's already obvious from the code. Focus on what's missing.

Type of docs needed: [README / inline JSDoc / API reference / function comment / full module docs]
Audience: [other devs on the team / open source users / beginners / seniors only]

Code:
[PASTE CODE]
```

---

## Variations

**For README generation:**
```
Write a README for this project. Sections: what it does (2-3 sentences max), installation, quickstart with a real example, configuration options, and when NOT to use this. Skip the "contributing" and "license" sections.

Project code/description:
[CONTEXT]
```

**For API endpoint documentation:**
```
Document this API endpoint for external developers. Include: what it does, request format with example, all possible response codes with what triggers each, and any rate limits or auth requirements.

[PASTE ROUTE HANDLER OR SPEC]
```

**For inline comments (when code is complex):**
```
This code is doing something non-obvious. Add inline comments that explain the WHY, not the WHAT. Assume the reader can read code — they just don't have the context I had when I wrote this.

[PASTE CODE]
```

---

## Notes

The "audience" field changes the output more than most people expect. Docs written for senior devs assume a lot; docs for beginners over-explain. Be specific.

The "don't document the obvious" rule is the hardest thing to get models to follow. If you get overly verbose output, add: "Remove any comment that just restates what the code already says."
