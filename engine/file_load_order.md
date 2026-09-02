# What loads, and in what order

_Written by the engine at the end of every session. Editing it by hand has
no effect — change the engine if the order should be different._

Each session, Eira is given the following, in this order. The start
and the end of a long prompt get the most attention, so the rules come first
and a short reminder comes last.

1. **`constitution.md`** — the rules that outrank everything, from the utility repo
2. **`operator-instructions/README.md`** — what the operator has asked for today, from the private repo
3. **`gift.md`** — the north star, from the utility repo
4. **`harness.md`** — how a session runs, from the utility repo
5. **`identity/soul.md`** — who the agent is
6. **`identity/voice.md`** — how the agent sounds
7. **`planning/goals.md`** — what the agent is working toward
8. **`identity/memory/`** — the memory folder: instructions, the short-term buffer, and
   the long-term index. The whole of any one memory is read only when the agent
   asks for it by id with `recall`
9. **`planning/open-questions.md`** — what is still open
10. **`directory.md`** — the map of the repository
11. **`(active carry)`** — files the agent chose to load this session, from the
   Active carry section in directory.md — up to two, capped at 4 000 chars
12. **`record/journal/ (last 3)`** — the most recent journal entries
13. **`record/emails/ (unread)`** — unread mail, from the private repo
14. **`(outbox count)`** — how many emails are waiting to be retried
15. **`tasks.json`** — open tasks, from the private repo
16. **`private_memory/working_memory/`** — what the last session read, searched and wrote
17. **`(budget)`** — worked out from operations/budget.json
18. **`(tools)`** — the actions available, and the scripts in operations/tools/
19. **`(how to act)`** — how the engine works, and the agent's own journal template
20. **`(current session)`** — which session this is, and the time
21. **`(remember)`** — a short reminder of identity and the rules, read last

Names in brackets are not files. They are assembled by the engine from
several places, or worked out rather than read.
