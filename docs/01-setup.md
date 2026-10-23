# Setup (about 20 minutes)

## What you need

- A paid Claude plan (Pro or Max). Max is worth it once you're using this daily.
- A Mac or Windows computer.

## 1. Install VS Code

Download it from https://code.visualstudio.com and install it.
It looks like a developer tool because it is one. You only need three parts of it:

- **Explorer** (left sidebar, top icon): the files in this folder.
- **Editor** (middle): where a file opens when you click it.
- **Claude Code panel**: where you chat.

## 2. Install the Claude Code extension

1. In VS Code, open the Extensions sidebar (the four-squares icon, or `Cmd+Shift+X` / `Ctrl+Shift+X`).
2. Search **Claude Code**. Install the one published by **Anthropic**.
3. Click the Claude icon that appears in the top right of the editor (or the sidebar) to open the panel.
4. Sign in with your Claude account when it asks.

## 3. Get this folder and open it

1. On the GitHub page for this repo, click **Code > Download ZIP** and unzip it. (If you already use git, clone it.)
2. Rename the folder to your business name and put it somewhere permanent, e.g. `Documents/acme-workspace`.
3. In VS Code: **File > Open Folder** and pick it.
4. Open the Claude Code panel. Claude now reads `CLAUDE.md` and can see every file in here.

Everything stays on your computer. Claude reads and edits these files when you ask, and it asks permission before doing anything risky.

## 4. Your first three prompts

Paste these one at a time.

```
Read README.md and CLAUDE.md, then give me a 5-bullet tour of this workspace and what I should do first.
```

```
Interview me to fill in the [brackets] in CLAUDE.md: my name, the business, and how I like to work. One question at a time. Keep it short.
```

```
Read docs/03-best-practices.md. Quiz me with 3 questions to make sure I got the important parts.
```

Then go to [prompts/01-seed-the-knowledge-base.md](../prompts/01-seed-the-knowledge-base.md).

## 5. (Optional, recommended) Back it up with GitHub

GitHub stores a copy of this folder and every change you make to it, so you can always roll back.

1. Make a free account at https://github.com.
2. Ask Claude: `Help me back this folder up to a private GitHub repo. Walk me through it step by step.`

After that, ask Claude to "commit and push" at the end of any session where you changed things.

## Things that trip people up

| Problem | Fix |
|---|---|
| Claude asks permission a lot | Normal at first. Approve things you understand. You can tell it "always allow" for safe ones like reading files. |
| Claude seems to have forgotten something | It only knows what's in this folder and the current chat. If it matters, save it to a file. |
| The chat is getting long and slow | Start a fresh chat. Everything important should already be in files. |
| You're not sure what Claude did | Ask: "What files did you change and why?" |
