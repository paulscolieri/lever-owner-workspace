# 04. Map one process end to end

Goal: one process mapped well enough that it could be handed to a new hire or built as a tool.

Shortcut: type `/map-process` in the chat. Or paste this:

```
Let's map [quoting / scheduling / invoicing] end to end. The file lives at knowledge/processes/[name].md.

Interview me one question at a time to fill in every section of knowledge/processes/_template.md:
- Trigger: what starts it, and where it shows up
- Steps, in order, with who does each one today and which software they touch
- Decision points: every "if X then Y," including the weird cases
- Information needed at each step and where it lives
- What "done" looks like
- Time spent and volume per month
- What goes wrong today

Then add a "Future state" section: for each step, mark it as
  - AUTO (a script can do it the same way every time),
  - AI DRAFT (Claude drafts, a person approves), or
  - HUMAN (stays with a person),
and explain why in one line each.

Finish with a simple diagram of the flow in a mermaid code block.
```

When it's done:

```
Read knowledge/processes/[name].md and write a one-page pilot brief: the problem, hours and cost today, what the tool would do, what stays human, risks, and what we'd measure in the first 60 days. Save it as knowledge/processes/[name]-pilot-brief.md.
```
