# [Business name] workspace

You are working with [your name], who owns [business name]. [One line on what the business
does, who it sells to, and where.]
This folder is the company's knowledge base and automation workspace.

## How to work with me

- I'm new to Claude Code and to code. Explain technical steps in plain language. When you run a command, say in one line what it does.
- Prefer short answers. Use lists and tables.
- When I describe how something works in the business, offer to save it to the right file in `knowledge/`.
- [Add your own: how you like answers, when to ask vs. decide, anything Claude keeps getting wrong.]

## Where things live

| Folder | What goes there |
|---|---|
| `knowledge/company/` | Who we are, team, partners, goals, the software we use |
| `knowledge/services/` | One file per service or product: what's included, how it's priced, what changes the price |
| `knowledge/processes/` | One file per business process, mapped with `knowledge/processes/_template.md` |
| `knowledge/vendors/` | Suppliers and subcontractors, who to call for what |
| `knowledge/policies/` | Rules customers ask about: deposits, cancellations, warranties, payment terms |
| `knowledge/calls/` | Call notes and transcripts |
| `knowledge/voice.md` | How we write to customers |
| `knowledge/roadmap.md` | Every process, ranked, plus the 12-18 month plan |
| `directives/` | SOPs for workflows Claude runs. See `directives/README.md` |
| `execution/` | Scripts those workflows call. See `execution/README.md` |

## Rules

- **Knowledge base is the source of truth.** Answer from `knowledge/` first. If the answer isn't there, say so and ask, then offer to save the answer.
- **One fact, one place.** Update the existing file instead of creating a near-duplicate.
- **Draft, don't send.** Anything that reaches a customer, vendor, or partner is a draft for a person to approve, unless I've said a specific workflow can send on its own.
- **Repeatable work becomes a script.** If a task needs the same steps and the same output every time, write a script in `execution/` and an SOP in `directives/` instead of doing it by hand in chat.
- **Secrets stay in `.env`.** Never write API keys, passwords, or card or bank details into any other file.
- **Customer personal data stays in the system it lives in.** Don't copy it into `knowledge/`. Look it up when needed.
- **Learn out loud.** When something breaks or I correct you, fix it, then update the relevant file here so it doesn't happen again.
