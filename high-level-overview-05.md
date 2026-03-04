---
author: Joel Singh
---

# DU Code Competition Group
Welcome to the third meeting!

Take the first 5 minutes to introduce your name and make some
small talk with the person you know least in the room.

Additionally, here's todays programming fun fact:

The empty string (c-style) and the empty character are NOT the same thing,
i.e ('' != ""). I realized this after dealing with a mysterious
bug that ended up being because I assumed that the empty string
and empty character are equivalent.

---

## Plan For Today

- Doing a high level overview of the DU Slither main function`

- Diving into the `compute_game_logic` function which handles
  the majority of the game logic. Pay attention, you'll conduct
  a small exercise where you make a change to the game logic.

- Matters of import concerning the upcoming DU Slither
  competition and the next one.

---

## Main Function Overview

- The main function holds all the state of the game, the cells,
  where the players are, the current game tick, etc.

- The main function uses SFML: https://www.sfml-dev.org/ , a
  multi-media library used to keep track of time and draw
  graphics.

- I will just go through the main function yapping about it.

---

## Compute Game Logic

- This function computes the logic of the game!
- As I yap think of something you could change such as:
    - Having the shortest snake win when time runs out
    - Disallow 2 length snakes being able to double back on
      themselves
    - Snakes no longer hit walls, they just stay in place
    - Or anything else in the same vein

You will program this as practice.

---

## Matters Of Import

- The Fall Competition. The fall programmatic game competition
  will feature a new game. What this new game actually is I
  don't know yet. An issue describing what the new game should
  be like is on Github. If anyone would like to take the lead on
  this one and design it let me know.

---

## End

- Next meeting will be Sunday, 7 to 8 pm once again
- As you have questions for practice, direct them to #competition-group-questions in discord. I'll be checking it regularly.
