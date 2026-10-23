# 06. Draft replies with a person in the loop

Goal: the copy-paste version of a customer assistant, usable today by you or someone on your team, before anything is connected to your software.

```
Here's a message from a [prospective / current] customer:

[paste message]

Context: [anything you know: who they are, past jobs, what they asked for before]

Draft a reply using knowledge/services/, knowledge/policies/, the right process in knowledge/processes/, and the tone in knowledge/voice.md. Then below the draft, list:
- the facts you relied on and which file each came from
- anything you weren't sure about
Don't promise anything that isn't in the knowledge base.
```

Once that works well, ask Claude to turn it into a skill so anyone on the team can type `/draft-reply`:

```
Turn the reply-drafting prompt I've been using into a skill called draft-reply in .claude/skills/. It should take a pasted message, work out which process it belongs to, follow that process file, and always show its sources and open questions under the draft.
```
