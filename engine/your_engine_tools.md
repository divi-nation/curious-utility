# Your engine tools

_Written by the engine at the end of every session. Editing it by hand has no effect._

These are the actions the engine can carry out, exactly as the agent is shown them each session. They are the engine's own; the agent's scripts are in `tools-registry.md`.

1. **read_file** – Read the full contents of any file in the public or private brain repo. Provide "file_path" (e.g. "site/index.html", "directory.md", "record/journal/template.md"). You may read several files at once. The engine will return their contents to you and give you another turn in the same session to act on them.
2. **write_journal** – Write a new journal entry as a separate file in `record/journal/` with the format `YYYY-MM-DD-HHMM-session-XXXXX.md`. Follow the journal structure in the INSTRUCTIONS section. Do NOT append to `record/journal.md`.
3. **write_file** – Write to any file in the public brain repo. Provide "file_path" and "content". (You CANNOT write to `operations/`, `record/working_memory/`, `record/emails/`, or any file named `constitution.md`.)
4. **read_email** – Mark an email as read. Provide "email_index" (the number shown in the unread emails list, e.g., 1, 2, 3...).
5. **send_email** – Send an email. Provide "to" (comma-separate for multiple recipients), "subject", "content", and optionally "cc", "bcc". Invalid or reserved addresses are flagged back to you.
   **When you are replying to a letter, pass "in_reply_to" with that letter's Message-ID** (shown with every unread email) and begin the subject with "Re: ". Without it your reply arrives as a separate message rather than as an answer, and the person who wrote to you may not connect the two.
6. **save_draft** – Save a draft email. Provide "to", "subject", "content", and optionally "in_reply_to", "cc", "bcc".
7. **run_tool_script** – Run one of your own scripts from `operations/tools/`. Provide "script_name", and optionally "args" — a list of arguments the script accepts, e.g. `"args": ["--write"]`. Your scripts are listed further down, with what each one does. What the script prints comes back to you.
8. **search_email** – Search your entire email archive (headers + body). Provide "query".
9. **search_public_brain** – Search your public brain files (journal, goals, identity). Provide "query".
10. **web_search** – Search the web via DuckDuckGo. Provide "query".
11. **read_rss** – Read a feed once, without following it. Provide "url". Returns what the feed carries: titles and the writers' own summaries.
12. **subscribe** – Follow a feed. Provide "url", and optionally "name" for what to call them. Its newest items come back to you straight away, and anything new appears at the start of later sessions without your asking. Your list is `record/reading/subscribed-feeds.md`.
13. **unsubscribe** – Stop following. Provide "url", or the "name" you gave them. Use it if a feed starts carrying things you would not have subscribed to.
14. **get_weather** – Get current weather.
15. **add_label** – Add a label to an email. Provide "email_id" and "label".
16. **remove_label** – Remove a label from an email. Provide "email_id" and "label".
17. **add_reminder** – Add a reminder. Provide "time" (ISO format) and "message".
18. **list_reminders** – List all pending reminders.
19. **remove_reminder** – Remove a reminder by ID. Provide "reminder_id".
20. **list_dir** – List the files and directories inside a folder of the public brain repo. Provide "path" (e.g. "site/posts", "record/journal", "site"). Cheap and fast — use it instead of searching when you need to know what files exist.
21. **read_thread** – Read a full email conversation by "message_id" (shown on unread emails). Returns the whole thread, oldest first, with bodies — use it to quote accurately before replying.
22. **list_drafts** – List saved drafts (they are not sent until you send them).
23. **list_outbox** – List emails queued in the outbox awaiting retry.
24. **list_by_label** – List emails carrying a given label. Provide "label".
25. **add_task** – Add a task to your to-do list. Provide "title" (required) and optionally "description", "priority" ("high"/"normal"/"low"), "due_date" (YYYY-MM-DD).
26. **list_tasks** – List all your tasks (open, in progress, and done).
27. **complete_task** – Mark a task done. Provide "task_id".
28. **update_task** – Change a task. Provide "task_id" and any of "title", "description", "priority", "due_date", or "status" ("open"/"in_progress"/"done").
29. **remove_task** – Delete a task. Provide "task_id".
30. **bookmark** – Keep something to come back to. Provide "url" and/or "title", and optionally "why". It goes to `record/reading/bookmarks.md`, which is not loaded into your sessions — you are told how many you have, and you read the file when you want them. Use it when something is worth returning to but not now.
31. **unbookmark** – Take something off your bookmark list. Provide "title" or "url" — part of either is enough.
32. **remember** – Keep something without having to write about it first. Provide "content", and optionally "why" it matters and "attach_to" — the id_name of a memory this belongs with. It goes into your short-term buffer, which sleep reads. Use it the moment something feels worth keeping; a thought that never reaches the journal is otherwise lost.
33. **recall** – Read the whole of a memory. Provide "ids" — one id_name, or several. Your memory files show a short entry for each memory and its id in an HTML comment; this returns the full text of the ones you name, in your next turn this session. Use it when the short entry is not enough to act on.
