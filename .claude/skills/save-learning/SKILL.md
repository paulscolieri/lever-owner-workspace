---
name: save-learning
description: Save a fact, rule, correction, or answer from the current chat into the right knowledge base file. Use when the owner says "save that", "remember this", or corrects something.
---

# Save a learning

1. Identify the fact in one or two sentences. If it's ambiguous, confirm the wording.
2. Find where it belongs in `knowledge/` (see `knowledge/README.md`). Search for an existing file that covers the topic first.
3. Update that file in place. Replace outdated info rather than adding a contradicting line. Create a new file only if no file covers the topic.
4. If it changes how Claude should behave everywhere, add one short line to `CLAUDE.md` instead.
5. Never save customer personal info or secrets.
6. Say in one line what changed and where.
