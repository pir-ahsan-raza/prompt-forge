# Code Review - Honest Feedback Mode

**Use when:** You want a real review, not validation. Especially useful when you've been staring at the same code for hours and your eyes stop seeing the problems.

---

## The Prompt

```
Review this code like a senior engineer who doesn't have time to be polite about it, but isn't mean either. Give me actionable feedback, not observations.

Specifically look for:
1. Logic errors or edge cases I'm probably not handling
2. Performance issues that will actually matter at scale (ignore micro-optimizations)
3. Security problems — especially input validation, auth assumptions, or data exposure
4. Places where the code will confuse the next person reading it (including future me)
5. Anything that'll break in prod that works fine locally

Format your response like this:
- **Critical** (fix before shipping): [issues]
- **Should fix** (tech debt that'll bite you): [issues]
- **Minor** (if you have time): [issues]
- **Actually fine**: [things that look weird but are deliberate — if any]

Don't rewrite the whole thing unless I ask. Point me at the problem, tell me why it's a problem, and let me fix it.

Language/framework: [SPECIFY]
Context: [WHAT THIS CODE DOES IN ONE SENTENCE]

Code:
[PASTE CODE]
```

---

## Variations

**Security-focused pass:**
> Ignore everything else. Only look for security vulnerabilities. Be paranoid.

**For a PR review:**
> I'm reviewing a PR from a junior dev. Give me talking points for the review conversation - frame issues as learning opportunities, not gotchas. Still be accurate.

**Quick sanity check:**
> I'm about to ship this. Does anything look obviously wrong? 60-second gut check only.

---

## Notes

The format matters. Without it you get a wall of prose where critical issues and nitpicks get equal weight, which is annoying.

Specifying language and context changes the output a lot - a Python data pipeline has different failure modes than a Node.js API route. Worth the extra two seconds.
