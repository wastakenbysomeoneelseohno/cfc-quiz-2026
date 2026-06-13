# CFC Quiz — How to use

Two apps, each a single page in your browser (Chrome works great).
Nothing to install. Nothing to run. Nothing leaves your computer.

| App | What it's for | Link |
|---|---|---|
| **Maker** | **Build** the question deck | https://wastakenbysomeoneelseohno.github.io/cfc-quiz-2026/maker.html |
| **Display** | **Run** the quiz on the day | https://wastakenbysomeoneelseohno.github.io/cfc-quiz-2026/display.html |

> ⚠ **Always Export to save your changes.** The browser auto-saves your work locally, but that lives only in
> *that* browser on *that* device — it can be lost by clearing site data, switching machines, or another person
> using the link. The **exported file is the real save**: Export after every editing session and keep the file.
> (You can also download `maker.html` / `display.html` and open them straight from a folder — they work offline.)
>
> ℹ The hosted links are updated **manually** and can lag behind this repository — if a feature described
> below is missing there, use the repo's `maker.html` / `display.html` directly (or redeploy).

---

## 1. Build your quiz (Maker)

The Maker has **three panels**: **Streams** (left) · **Slides** (middle) · **Slide options** (right).

1. **Open the Maker** (link above) and **name your quiz** in the box at the top (used for the saved file name).
2. **Streams** are **separate quiz tracks** in the same file — e.g. a **Main Quiz**, an **Audience Round**,
   or a **segue / interlude**. **+ Stream** adds one and opens **✎ Stream settings** — name it and set the
   **defaults new questions start with** (timer, timer-start, points, show-answer-screen, scored, auto-next). Double-click a name for a quick rename; **↑ / ↓** on a row reorders the streams.
   - All streams in a deck **share one scoreboard and one team count** (the same teams play every track).
   - **🪧 Header / footer** (next to 👥 Teams): give the show a **small logo + title**, always **centered**
     in a reserved header band at the top (the timer ring and slide content start below it), and a
     **footer note + small footer logo** (bottom left, above the controls). A **blank title uses the deck
     name**; colors follow the theme; leave everything blank and no band is reserved at all.
     **Logo sizing:** an SVG is ideal; for PNG export the header logo around **88–128 px** tall
     (shown ≤44 px) and the footer logo around **52–64 px** tall (shown ≤26 px), transparent background,
     under ~50 KB — images are stored inside the deck file.
   - The **deck name becomes the browser tab title** in both the Maker and the Display.
   - Set the **👥 Teams** count once, on the Streams panel — it applies to the whole deck.
   - During the show you can **switch between streams** and come back where you left off.
3. **Add slides** with **+ Slide**:
   - **Question** — pick a **format** and switch it any time:
     **Multiple choice**, **True / False**, **Short Answer** (type a word or a number),
     **Question with Title**, **Picture**, **Matching**, **Poll**, **Buzzer**.
   - **Title** — a heading or round divider. Its **subheading** is a multi-line box — good for instructions/rules.
   - **Leaderboard** — shows every team and its score as a clean table.
   - **Podium (Winners)** — the finale: top 3 on a gold/silver/bronze podium (with a 👑 crown) and
     **everyone else in a side table**.
   - **Reveal Answers** — an **answer browser**: it steps through the answer screens of every question
     **before it** in the stream (back to the previous Reveal Answers slide — so one per round works),
     with **◀ ▶ arrows**, a **“4 / 12” counter**, an optional **auto-advance every N seconds** (default 10,
     0 = manual; **⏸/▶** to pause; a **loading bar** fills toward the next answer — on the **last** answer
     the countdown stops, and **▶** there plays again from the first) and a **Loop** option that starts
     over automatically.
     Perfect with “Show answer screen: No” questions — their answers appear here instead.
4. **Fill in the question and answer.** Per question you can set (new questions inherit the stream's defaults):
   - the **timer** (on/off; 10s up to 7 minutes) and whether it **auto-starts** or **starts on a button**,
   - the **Points** it's worth (✓ adds them, ✗ subtracts them),
   - **Show answer screen: Yes / No** (default **No**) — **Yes** adds an answer slide after the question.
     With **No**, a **Reveal Answers** slide later can still show the answer (decks saved before this option
     existed keep their answer screens automatically),
   - **Scored: Yes / No** — set **No** for warm-ups / audience / tie-break questions; they show **no scoring page**,
   - **Auto next: Yes / No** (default **No**) — **Yes** = when the timer hits 0, the show **advances by itself**
     after a ~2.5s beat (to the answer screen / scoring / next slide, whichever comes next per the flags above).
     **+5s** after Time's-up revives the timer and cancels the pending hop.
5. **Drag slides** to reorder. **Preview** any time with **P** or **▶ Present**.
6. **Save it — always Export:** **Export** offers two formats — **★ 🔒 JSON** (the recommended save: password-locked, hides the answers) or **CSV** (a spreadsheet file you can edit in Excel/Sheets; carries questions, defaults and themes — answers are visible). **Import** reads either back, and **Merge is smart**: a stream with the **same name replaces** the old one, new names are added — so you can build one deck from several CSVs and re-import after edits without duplicates. In the CSV, each thing is a **heading row then a value row** (`[DECK]`, `[STREAM]`, `[SLIDES]`); a question's blank timer/points/reveal/scored/auto takes the **stream's default**, and the correct option is marked with `*`.

> Your work is auto-saved in the browser. **🗑 Reset** wipes the Maker's own data and reloads the sample deck
> (it never touches a Display running in the same browser).
>
> **On a phone/tablet** the Maker becomes a drill-down: **Streams → tap a stream → its questions → tap a question → edit**, with **← back** buttons.

---

## 2. Run your quiz (Display)

1. **Open the Display** (link above) on the screen/projector everyone sees.
2. **Load your quiz file** and **type the password** to unlock it.
3. **Choose the stream** and the **number of teams** (shared by all streams), then press **▶ Start show**.
4. **Move through the quiz:**
   - **Click and hold** the big button (~0.8s) **with your mouse** to advance or reveal the answer.
     Holding prevents accidental clicks. The button always **names the next page**. There are **no keyboard shortcuts** — every action is an on-screen button (Esc does **not** exit).
   - On a timed question the answer unlocks **after the timer ends**. Use **−5 / +5** to adjust, or **⏰ Time's up** to end it now.
   - Use **← Back** to step back. A small **Q 3 / 12** label (top-left) shows which question you're on.
   - The bottom control bar **scrolls left/right** if it's wider than the screen.
5. **Give points:** after a question, tap each team **✓** or **✗** (worth the question's **Points**) — marked teams light up
   **green / red**. No submit step: marks are **saved automatically when you move on** (advance, switch streams, or exit). The score console shows committed scores only — it notes when marks are still pending on the current slide.
6. **Switch streams** with the dropdown — it remembers where you left off in each; the scoreboard carries across them.
7. **Resume:** reopening the same file later offers **⏯ Continue where you left off** (scores kept) or **↺ Start fresh**.

### 🔒 The private Score Console (operator only)

The projector mirrors your screen, so you should **never edit scores on the projected window**. Instead:

> **Click the 🏆 Scores button** → a **separate popup window** opens. Drag it to your **own laptop screen**
> (the one the audience can't see). It lists **every team in order** with **− / +** and a **set-to-a-number** box,
> shows the **deck and stream** you're editing, and notes if a question has **marks still pending** (those only
> count once you advance). Changes are **live** — if a Leaderboard or Podium slide is up, it updates too.
> Closing the popup is fine — clicking 🏆 again re-opens it. Exiting the show closes it.
> *(If your browser blocks pop-ups, allow them for this page.)*

> **🔑 Secret: jump to any slide.** Hold **Ctrl** (**⌘ Cmd** on Mac) and **click 🏆 Scores**. A panel shows
> **slide numbers only** (no questions, so nothing leaks). Click a number to peek, then **▶ Go** to jump there.

That's it. Build in the Maker, **Export** (your real save), open the file in the Display, and run the show.

---

## For developers

- **Single-file, no-server** apps; state in `localStorage`, content moves as files. Maker keys are `m_`-prefixed,
  Display keys `d_`-prefixed — the two never share storage.
- **Tests** (need Chrome + `npm i puppeteer-core`): `node test.js` runs everything; or `node test.unit.js` /
  `node test.integration.js` / `node test.e2e.js`. See `SPEC.md` for the design.
