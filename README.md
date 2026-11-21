# English Escape Rooms 🚁

**Eight escape rooms for A2–B1 learners — one per class group.** Every group
plays the same challenges and learning objectives through a *different travel
story*: a single self-contained HTML file with no dependencies. A friend gets
hurt on an adventure, and only English can save the day — solve every room,
collect the letters, and enter the rescue code.

## Play

Open `index.html` in any browser, or visit the published site:

**https://profemanu1999-prog.github.io/english-games/**

The start page is a **lobby** where each group picks their adventure.

### Direct links for each group

Share these so students land straight in their own escape room:

| Group | Link suffix | Adventure | Friend | Code word |
| ----- | ----------- | --------- | ------ | --------- |
| 1 | `/#1` | 🏔️ The Mountain Rescue | Sam | RESCUED |
| 2 | `/#2` | 🐪 The Desert Caravan | Omar | CARAVAN |
| 3 | `/#3` | 🌴 The Amazon Expedition | Ravi | EXPLORE |
| 4 | `/#4` | ❄️ The Arctic Station | Nina | GLACIER |
| 5 | `/#5` | ⛵ The Island Storm | Tom | SURVIVE |
| 6 | `/#6` | 🏛️ The Lost City Trek | Zara | TEMPLES |
| 7 | `/#7` | 🛶 The River Rapids | Diego | CURRENT |
| 8 | `/#8` | 🐘 The Safari Rescue | Amara | RANGERS |

Example: `https://profemanu1999-prog.github.io/english-games/#5` starts
Group 5's adventure immediately (`#group-5` also works).

Sound: the listening room uses the browser's built-in text-to-speech. If a
device has no speech voices, the radio messages are shown as text instead.

## Rooms & learning objectives (identical in every story)

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

Each room awards one letter; together they spell that story's code word.

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

- `CONFIG` — title, level, pacing, speech rate.
- `STORIES` — the eight adventures. Each entry has the story (friend,
  setting, accident, rescuer, code word) and its eight rooms. Change
  vocabulary, sentences or story text freely — the engine adapts. To add a
  ninth group, copy a story block, change `name`, `group`, `codeWord` and
  the content; the lobby and direct links update automatically.

## Publish updates

The folder is already live via GitHub Pages — updates are one push:

```sh
git add .
git commit -m "Update games"
git push
```

Pages rebuilds automatically (usually within a minute or two).
