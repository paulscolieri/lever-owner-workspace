# How this works

## Four ideas

1. **Knowledge** (`knowledge/`): how your business runs, written down as plain text files. Services and pricing, processes, vendors, policies, how you talk to customers. Claude knows everything in the world except your business. This is where it learns yours.
2. **Skills** (`.claude/skills/`): your repeatable processes saved as commands. Type `/` in the chat to see them.
3. **Tools** (`.env`): keys to the software you already pay for (CRM, accounting, email, calendar, Slack). Most of it has an API, which is a door Claude can use instead of you clicking around.
4. **Code** (`directives/` and `execution/`): for anything that has to come out the same way every time, Claude writes a small script and runs that instead of improvising.

Put them together and "a customer emailed asking for a quote" becomes:

> Read the email → check `knowledge/services/` for how that job is priced → check `knowledge/processes/quoting.md` for what to ask before quoting → draft the quote and the reply in the tone in `knowledge/voice.md` → you review and send.

What used to take 20 minutes of looking things up takes 2 minutes of reviewing.

## Why not just use Claude in the browser?

| Browser chat | Claude Code in this folder |
|---|---|
| Context lives in one chat and gets lost | Context lives in files and is always there |
| New chat means starting over | New chat, same knowledge, picks up where you left off |
| Can't run anything | Writes and runs scripts, on a schedule if you want |
| The same question can get a different answer each time | Repeatable work becomes a script with the same output every time |

That last row is the big one.

## Judgment vs. scripts

AI is good at judgment: reading a messy customer message, working out what they want, writing a friendly reply.
AI is not reliable at doing 10 steps exactly the same way 500 times.
Code is.

So the system splits work in two:

- **Directives** (`directives/`): plain-English SOPs. "When a quote request comes in, do steps 1-6." Claude reads these and makes the judgment calls.
- **Execution** (`execution/`): scripts Claude writes for the mechanical steps. "List tomorrow's jobs from the calendar." "Pull this month's unpaid invoices." Same input, same output, every time.

You don't write either one. You describe the process, Claude writes the SOP and the scripts, you review.

## How it grows

- **Weeks 1-4**: knowledge only. Claude answers questions and drafts from what you've written down.
- **Months 2-3**: one process mapped end to end. That's your pilot.
- **After that**: connect the software that process touches, script its mechanical steps, add a schedule ("every Monday at 8am, send me this week's jobs"). Then the next process on the roadmap.

## Skills

This workspace starts with two:

- `/map-process`: interviews you about a process and writes the map.
- `/save-learning`: saves something you just figured out into the right knowledge file. "Save that" does the same.

When you catch yourself typing the same instructions twice, ask Claude to turn them into a skill.

## GitHub

Optional, and worth it once the folder matters to you. GitHub keeps a copy of the folder and every change ever made to it, so a bad edit is one command to undo. When someone joins the team, they pull the same folder and their Claude knows what yours knows. [docs/01-setup.md](01-setup.md) step 5 sets it up.
