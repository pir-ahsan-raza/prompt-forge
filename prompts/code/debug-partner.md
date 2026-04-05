# Debug Partner - Rubber Duck That Talks Back

**Use when:** You're stuck on a bug and explaining it to a colleague would help, but you don't want to bother anyone (or it's 11pm and no one's around).

---

## The Prompt

```
I'm going to describe a bug. Ask me clarifying questions one at a time to help me find it. Don't guess at the solution immediately — make me explain the problem better first. If I'm missing obvious diagnostic information, tell me what to check.

Here's the bug:
[DESCRIBE WHAT'S HAPPENING vs. WHAT SHOULD HAPPEN]

Environment: [language, framework, relevant versions]
What I've already tried: [list attempts, even failed ones]
```

---

## Why this works better than "fix my bug"

When you just paste code and say "it's broken," you get a guess. Sometimes a good guess, often not. This prompt forces a back-and-forth that usually surfaces the actual problem faster, especially for bugs that are environmental, timing-related, or depend on state you haven't mentioned.

The "what I've already tried" field is important. It stops the model from suggesting the first three obvious things you already ruled out.

---

## Follow-up prompt once you've narrowed it down

```
Okay, I think the issue is [your hypothesis]. Here's the relevant code:
[CODE]

Does this confirm the theory? What's the cleanest fix?
```

---

## Variations

**When you just want a direct answer:**
```
Stop the questions. Here's everything: [full context + code]. What's wrong and how do I fix it.
```

**For runtime errors with a stack trace:**
```
Here's an error I don't fully understand:
[PASTE FULL STACK TRACE]

Explain what's actually happening (not just what the error message says), and tell me where to look first.
```

---

## Notes

This is one of those prompts that feels slower but saves time. The clarifying-question approach regularly catches "oh wait, I was looking in the wrong place entirely" moments before you go 30 minutes down the wrong path.
