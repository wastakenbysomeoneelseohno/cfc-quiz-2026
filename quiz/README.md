# Quiz folder

Put your exported decks here — plain **`.json`** or encrypted **`.cfcq.json`** files from the Maker.

When you open the **Display over http** (a local server or the hosted link), every deck in this
folder shows up in the **"Load from the quiz folder"** dropdown — pick one, type the password if it's
encrypted, and start. (You can always **drag & drop** a file instead — both options are always there.)

## Important: it must be SERVED, not double-clicked
Browsers block a `file://` page from reading a folder, so if you **double-click `display.html`** the
dropdown stays **empty** and you just drag & drop. To get the dropdown, serve the project folder, e.g.:

```
# from the project root (where display.html lives):
python -m http.server 8000
# then open:  http://localhost:8000/display.html
```

(or `npx serve`, VS Code "Live Server", etc.)

## How decks are listed
The Display tries, in order:
1. **`quiz/manifest.json`** — an optional list you maintain, e.g. `["adult-quiz.cfcq.json", "kids.json"]`
   (most reliable; survives any server).
2. Otherwise it parses the **server's directory listing** of `quiz/` (works with `python -m http.server`,
   nginx autoindex, etc.) — so usually you don't need a manifest at all; just drop files in.
