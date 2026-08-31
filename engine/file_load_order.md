# What loads, and in what order

_Written by the engine at the end of every session. Editing it by hand has
no effect — change the engine if the order should be different._

Each session, Eira is given the following, in this order. The start
and the end of a long prompt get the most attention, so the rules come first
and a short reminder comes last.

1. **`authority.md`** — which file wins when two of them disagree, from the utility repo
2. **`constitution.md`** — the rules that outrank everything, from the utility repo
3. **`instructions.md`** — what the operator asks of a session, from the utility repo
4. **`operator-instructions/README.md`** — what the operator has asked for today, from the private repo
5. **`gift.md`** — the north star, from the utility repo
6. **`harness.md`** — how a session runs, from the utility repo
7. **`identity/soul.md`** — who the agent is
8. **`identity/voice.md`** — how the agent sounds
9. **`planning/goals.md`** — what the agent is working toward
10. **`identity/memory/`** — the whole memory folder: instructions, short-term buffer, long-term
11. **`planning/open-questions.md`** — what is still open
12. **`directory.md`** — the map of the repository
13. **`record/journal/ (last 3)`** — the most recent journal entries
14. **`record/emails/ (unread)`** — unread mail, from the private repo
15. **`(outbox count)`** — how many emails are waiting to be retried
16. **`tasks.json`** — open tasks, from the private repo
17. **`private_memory/working_memory/`** — what the last session read, searched and wrote
18. **`(budget)`** — worked out from operations/budget.json
19. **`(tools)`** — the actions available, and the scripts in operations/tools/
20. **`(how to act)`** — how the engine works, and the agent's own journal template
21. **`(current session)`** — which session this is, and the time
22. **`(remember)`** — a short reminder of identity and the rules, read last

Names in brackets are not files. They are assembled by the engine from
several places, or worked out rather than read.
