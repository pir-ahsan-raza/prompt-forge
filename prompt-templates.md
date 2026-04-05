# Prompt Templates

Reusable structures I keep coming back to. Not fill-in-the-blank fluff -
actual patterns that change how the model responds.

---

## The Role + Constraint Template

Best for: getting focused, non-generic answers
You are a [specific role] with [relevant background].
I need help with [task].
Constraints:

[what to avoid]
[format preference]
[tone or length]


The constraint block is the part most people skip. It's also the part that
matters most.

---

## The Before/After Template

Best for: rewrites, feedback, editing
Here's what I have:
[original]
Here's what I'm going for:
[goal / intended effect]
What's not working and how would you fix it?

Gets you diagnostic feedback instead of just a rewritten version you may or
may not agree with.

---

## The Rubber Duck Template

Best for: debugging, thinking through a problem
I'm trying to [goal].
Here's what I've tried:

[attempt]
[attempt]

Here's where I'm stuck:
[specific blocker]
Don't give me the answer yet - ask me questions that help me find it.

Underrated. Forces the model into Socratic mode instead of answer-dump mode.
Works surprisingly well for logic problems.

---

## The Strict Output Template

Best for: automation, parsing, n8n/Make workflows
Extract the following from the text below.
Return ONLY a JSON object with these keys:

name
date
action

No explanation. No markdown. No extra keys. If a field is missing, use null.
Text:
[input]

Removing "no explanation, no markdown" causes half your automation workflows
to break. Keep it.

---

## The Steelman Template

Best for: stress-testing an idea before committing to it
I'm planning to [idea/decision].
Give me the strongest possible argument against this. Not a balanced take -
the best case for why this is a bad idea.
Then tell me what would need to be true for that argument to be wrong.

More useful than asking "what do you think?" which gets you a diplomatic
non-answer.

---

## The Chain of Thought Trigger

Best for: math, logic, multi-step reasoning
Think through this step by step before giving me the final answer.
[question]

Three seconds to add, meaningfully better output on anything that involves
reasoning. Just use it.
