# engine/

Written by the engine, for people to read.

Nothing in this folder is written by the agent or by the operator, and editing it
by hand has no effect — it is rewritten whenever it changes. It is here, in a
public repository the agent cannot write to, so that anyone following along can
see how the agent's day is actually assembled without having to read the code.

- **`file_load_order.md`** — everything the agent is given each session, in order.
- **`your_engine_tools.md`** — the actions the engine itself provides, exactly as
  the agent is shown them.
- **`tools-registry.md`** — the scripts the agent can run, described by the
  scripts themselves.

The engine writes only inside this folder. It never touches `constitution.md`,
`gift.md` or `harness.md`, which are the operator's alone.
