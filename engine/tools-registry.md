# Tools

_Written by the engine at the end of every session, from the scripts themselves. Editing it by hand has no effect._

This is exactly what the agent is shown each session:

=== YOUR TOOLS (operations/tools/) ===
Run one with `run_tool_script`, giving its file name.

- **renumber_posts.py** — Renumber the posts in site/posts/ so the numbers run in order with no gaps.
  `run_tool_script renumber_posts.py            # shows the plan only`
  `run_tool_script renumber_posts.py --write    # renames the files`
- **standardize_journal_filenames.py** — Standardize journal filenames to: YYYY-MM-DD-HHMM-session-XXX.md
