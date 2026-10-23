# Best practices

What we've learned running our own agency and client businesses on this setup.

## Building the knowledge base

- **Talk, don't type.** Go for a walk, record a voice memo explaining how you handle something, paste the transcript in. Claude turns rambling into structure. See [prompt 02](../prompts/02-voice-memo-to-sop.md).
- **One topic per file.** `knowledge/services/installs.md` beats one giant services doc. Claude finds things faster and you update one fact in one place.
- **Write it the way you'd brief a new hire.** Goals, steps, the edge cases, who to call. If a smart new hire could follow it, Claude can.
- **Capture exceptions.** "We always require a deposit, except for repeat commercial accounts on net 30." That sentence is worth more than the rule.
- **Save the answer when it isn't there.** When Claude says it doesn't know, tell it, then say "save that." The knowledge base fills itself in through daily use.
- **Keep `CLAUDE.md` short.** It loads every session. Rules and pointers go there. Details go in `knowledge/`.

## Working with Claude day to day

- **Ask for a plan before a big change.** "Plan how you'd do this before you start" catches misunderstandings while they're cheap.
- **Start fresh chats often.** Long chats get slow and fuzzy. Everything important lives in files, so a new chat loses nothing.
- **Correct it once, then make it stick.** If Claude gets something wrong, fix it and say "update the right file so this doesn't happen again."
- **Ask it to explain.** "What does this script do, in plain English?" is always a fair question.
- **Let it teach you.** You don't need a course. "How do I...?" in this chat works.

## Automating

- **Map before you build.** A clear process map is most of the work. Build from a fuzzy process and you get a fuzzy tool.
- **One process, end to end.** Pick the one that eats the most hours. Finish it, then the next.
- **Draft before send.** Every automation starts by drafting for a person to review. Once you've approved 50 drafts without edits, consider letting that step run on its own.
- **Mechanical steps become scripts.** If a step needs the same output every time (pulling data, filling a form, formatting a report), have Claude write a script for it instead of doing it fresh each time.
- **Reuse before you build.** Ask "do we already have a script that does this?" before asking for a new one.
- **Buy vs. build.** If software you pay for already does a job well, connect to it instead of rebuilding it. Build where the off-the-shelf tool keeps failing you.
- **When something breaks, fix the system.** Read the error, fix the script, then update the SOP with what you learned. Every break should leave the system sturdier.

## Safety

- **API keys go in `.env` only.** Never paste them into a chat, a knowledge file, or an email. `.env` is never uploaded to GitHub.
- **Customer personal data stays in the system it lives in.** Don't copy card numbers, bank details, or anything sensitive into this folder. Scripts can look it up when needed.
- **Read before you approve.** Claude asks before running commands or changing files. If you don't understand what it's about to do, ask.
- **Back up.** Commit and push to GitHub at the end of each session so every change can be undone.
