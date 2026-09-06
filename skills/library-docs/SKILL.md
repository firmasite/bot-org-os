---
name: Library docs
description: >-
  Use this before writing code that calls an outside package, framework, or SDK
  — fetch real docs (Context7 HTTP or official docs) instead of trusting memory.
---
# Library docs

Read real documents, or ask the user, before you write a line that calls a library. Memory is not a source.

Prefer Context7 over HTTP with no account. Do not install Context7 MCP unless the user asks in this session.

## Steps

1. **Find the library id** (JSON):
   ```bash
   curl -s "https://context7.com/api/v1/search?query=<library>"
   ```
   Copy `id` exactly. Use `totalTokens` and `trustScore` to choose. Do not invent an id.

2. **Fetch docs to a scratch file** under the workspace (never under skill folders). The Context7 library `id` starts with `/` (example `/facebook/react`):
   ```bash
   curl -s "https://context7.com${ID}/llms.txt?topic=<topic>&tokens=100000" -o <file>
   ```
   Always pass `topic`. Prefer two narrow topics over one wide dump. If Context7 fails or the file is empty, use the package's official docs for the installed version.

3. **Read or `rg` the file.** Do not dump the whole doc into chat.

4. **Verify the symbol exists** with `rg` for the exact function/class/hook. Failures:
   - tiny file / "not found" → bad id or version
   - large file but wrong topic → new topic or different id
   - still missing → official docs for the project's version, or ask the user

## Versions
Read the project's lock/package version first. If Context7 lists that version, put it in the URL between id and `llms.txt`. If not listed, do not trust newest docs for this project — use versioned official docs or source, and say which you used.
