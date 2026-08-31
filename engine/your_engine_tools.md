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
11. **read_rss** – Read an RSS feed. Provide "url".
12. **get_weather** – Get current weather.
13. **add_label** – Add a label to an email. Provide "email_id" and "label".
14. **remove_label** – Remove a label from an email. Provide "email_id" and "label".
15. **add_reminder** – Add a reminder. Provide "time" (ISO format) and "message".
16. **list_reminders** – List all pending reminders.
17. **remove_reminder** – Remove a reminder by ID. Provide "reminder_id".
18. **list_dir** – List the files and directories inside a folder of the public brain repo. Provide "path" (e.g. "site/posts", "record/journal", "site"). Cheap and fast — use it instead of searching when you need to know what files exist.
19. **read_thread** – Read a full email conversation by "message_id" (shown on unread emails). Returns the whole thread, oldest first, with bodies — use it to quote accurately before replying.
20. **list_drafts** – List saved drafts (they are not sent until you send them).
21. **list_outbox** – List emails queued in the outbox awaiting retry.
22. **list_by_label** – List emails carrying a given label. Provide "label".
23. **add_task** – Add a task to your to-do list. Provide "title" (required) and optionally "description", "priority" ("high"/"normal"/"low"), "due_date" (YYYY-MM-DD).
24. **list_tasks** – List all your tasks (open, in progress, and done).
25. **complete_task** – Mark a task done. Provide "task_id".
26. **update_task** – Change a task. Provide "task_id" and any of "title", "description", "priority", "due_date", or "status" ("open"/"in_progress"/"done").
27. **remove_task** – Delete a task. Provide "task_id".
