# Owner workspace

A folder on your computer that Claude Code works inside. Your business is written down in
it, your repeatable processes are saved in it, and Claude reads all of it before it
answers. Close the chat, open a new one tomorrow, and it still knows how you quote a job.

From the video: How to Use Claude Code to Run a Business (Even If You Don't Write Code)
(link added when it's live)

## The four ideas

```
                       SKILLS
             your processes, written like
               a brief to a new hire
                         |
                         v
  KNOWLEDGE   -->     CLAUDE     <-->   TOOLS
  your business,                        the software you already pay for:
  written down                          CRM, books, email, calendar
                         |                 ^
                         v                 |
                       CODE  --------------+
               same input, same output,
                     every time
```

| Idea | Folder | What goes in it |
|---|---|---|
| Knowledge | `knowledge/` | How the business runs: services and pricing, processes, vendors, policies, how you write |
| Skills | `.claude/skills/` | Saved commands. Type `/map-process` and Claude runs the whole interview |
| Tools | `.env` | Keys to your software, so Claude can read your calendar or CRM. Never uploaded anywhere |
| Code | `directives/` + `execution/` | A written SOP, and the scripts Claude writes for the steps that must come out the same every time |

Claude does the judgment work: reading a messy customer email, drafting the reply. Code
does the mechanical work. A person reviews and hits send.

## Start here

1. [docs/01-setup.md](docs/01-setup.md): install VS Code and Claude Code, open this folder. About 20 minutes.
2. [docs/02-how-this-works.md](docs/02-how-this-works.md): what each folder is for.
3. [docs/03-best-practices.md](docs/03-best-practices.md): the habits that make this work. Read it twice.
4. [prompts/](prompts/): copy-paste prompts, in order. Start with `01`.

## The first 60-90 days

| Step | What | You end up with |
|---|---|---|
| 1 | Setup and the first prompts | Claude Code running in this folder |
| 2 | Talk the business into it ([prompt 01](prompts/01-seed-the-knowledge-base.md), [02](prompts/02-voice-memo-to-sop.md)) | `knowledge/` filled in |
| 3 | List every process ([prompt 03](prompts/03-process-inventory.md)) | `knowledge/roadmap.md`, ranked |
| 4 | Map one process end to end ([prompt 04](prompts/04-map-one-process.md)) | A map good enough to hand to a new hire or build from |
| 5 | Automate that one process ([prompt 07](prompts/07-first-automation.md)) | Your first workflow, drafting for you to approve |

You don't build anything in steps 1-4. A clear map of one process comes first, and
building is faster and cheaper once it exists.

## Folder map

```
CLAUDE.md          Claude reads this at the start of every session. Keep it short.
docs/              How to use this workspace.
prompts/           Starter prompts to paste into Claude Code.
knowledge/         Your business: company, services, processes, vendors, policies, calls.
directives/        SOPs for workflows Claude runs. Empty until you automate something.
execution/         Scripts Claude writes for those workflows. Empty until then.
.claude/skills/    Saved commands, e.g. /map-process.
.env.example       Where API keys go. Copy it to .env. Never commit .env.
```

## What's not in here

Our own knowledge files. The folder structure is the easy part to copy. What makes it
work is months of answering "save that" every time Claude didn't know something, and
that has to be yours.

## License

MIT. Built by [Lever Agency](https://leveragency.ai). Use it for your business or your
clients. Attribution appreciated, not required. Stuck? Email paul@leveragency.ai.
