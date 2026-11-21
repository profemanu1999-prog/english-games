# The Mountain Rescue 🚁

An English escape room for **A2–B1** learners: a single self-contained HTML
file with no dependencies. Your friend Sam falls on a mountain trail — solve
every room, collect the letters, and call the rescue helicopter.

## Play

Open `index.html` in any browser (double-click), or serve the folder:

```sh
python3 -m http.server 8000   # or any static server
```

Sound: the listening room uses the browser's built-in text-to-speech. If a
device has no speech voices, the radio messages are shown as text instead.

## Rooms & learning objectives

| Room | Objective | Mechanic |
| ---- | --------- | -------- |
| 🎒 Pack Your Bag | Travel, adventure activities, packing essentials | Word sort (take / leave) |
| 🧭 Finding the Way | Distances and specific locations | Multiple-choice quiz |
| 🚑 What Happened? | Reporting events — past tense | Fill-in-the-blank with word bank |
| 🤕 What's Wrong? | Health conditions and injuries | Matching pairs |
| 💊 Get Help | Advisability, necessity, obligation (should / must / need to) | Multiple-choice quiz |
| 🗣️ Make a Plan | Asking for and responding to suggestions | Choose the best reply |
| 🔊 Say That Again | Listening and requesting repetition | Audio quiz (🔊 replay) |
| 🚁 The Rescue Code | Final puzzle | Unscramble the collected letters |

Each room awards one letter; together they spell the final code word.

**Quiz rooms use a mastery rule:** a wrong pick is marked with ✗ and that
question comes back in a **retry round** ("⚠️ You made some mistakes!") — the
room only opens when every question is finally answered correctly. Wrong
picks **stay eliminated**: when a question returns, its rejected options are
still ✗-marked and unclickable, so the same answer can't be chosen twice.
The correct answer stays hidden on the first miss (so the retry is a real
second chance) and is revealed ✓ after a second miss, to be tapped to
continue. Mistakes are also collected into a "words & phrases to review"
list on the final screen. No timers, no fail states.

## Edit the content

Open `index.html` and find the two marked blocks near the top of the script:

- `CONFIG` — title, level, code word, pacing, speech rate.
- `ROOMS` — the story and every room's items. Each room entry explains which
  fields its mechanic uses (`items`, `text`, `pairs`). Change vocabulary,
  sentences or story text freely — the engine adapts.

## Publish on GitHub Pages

The folder is ready to push as-is (an `index.html` at the repo root is all
GitHub Pages needs):

```sh
git init -b main
git add .
git commit -m "Add The Mountain Rescue"
gh repo create english-games --public --source=. --push

# enable Pages
gh api repos/{owner}/english-games/pages \
  --method POST -f source[branch]=main -f source[path]=/
```

Or via the web UI: **Settings → Pages → Deploy from branch → main / (root)**.

Add more games later as extra `.html` files and link them from an `index.html`
hub (use relative links).
