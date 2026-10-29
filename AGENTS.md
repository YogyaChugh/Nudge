# This is an AnyStudio app

The app is described in JSON documents that AnyStudio compiles to a Kotlin Multiplatform project (Android, iOS
and desktop):

- `app.json`: the app (name, theme, types, state, endpoints) and the lists of its screens and flows
- `*.screen.json`: one screen each; `*.flow.json`: one flow (what happens when something is tapped or arrives)
- `*.component.json`: parts shared by every screen
- `images/`: the app's own pictures
- `.studio/`: the Studio's own files (notes, tests, sample data, checkpoints); not part of the app

## How to change it

Use the AnyStudio MCP tools (`anystudio mcp install` sets them up for Claude Code, Codex and Cursor). Every edit
through them is checked, can be undone, and shows at once in an open Studio. Start with app_check to see the
app's problems, and catalog_fits before using a capability you are not sure exists. Editing the JSON by hand
works too: the Studio picks the change up, and `anystudio app app.json check` says what is wrong.

## Notes

`.studio/memory.md` holds short notes about the app: read it first, and add one line with memory_note when you
make a decision or finish a piece of work.
