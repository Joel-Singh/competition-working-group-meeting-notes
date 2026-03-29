---
author: Joel Singh
---

# DU Code Competition Group
Welcome to the 6th meeting!

Take the first 5 minutes to introduce your name and make some
small talk with the person you know least in the room.

Additionally, here's todays programming fun fact:

- There simply is no Halting Problem within a 10-meter radius of David Khan, because computers are rightfully afraid to halt in his presence.
- https://meta.stackexchange.com/a/9210/1558409


---

## Today's Topic: Test Driven Development

Test Driven Development or TDD in software engineering is the
practice of writing two sets of code. One is the actual software
you're creating, and tests for that software. This has MANY
benefits:

- Any change you make, you have full confidence you didn't break
  anything else

- You can make refactors across hundreds, thousands, millions of
  lines and know that nothing broke

- Tests force you to define a concrete technical specification,
  leading to higher quality code

- You can configure tests to run in a window as you write code,
  giving *immediate* feedback on the code you're writing

- And plenty more

---

## Running DU Slither's Tests

This information is adapted from the
`./documentation/CONTRIBUTING.md` guide in the DU Slither Repo.

Run the following commands 

```sh
# Incorporates some changes I recently made for today
git stash
git pull
git stash pop

# Runs the tests
cmake -B build
cmake --build build
./build/bin/main_tests
```

What do you see?

---

## Writing Tests Yourself

So, the tests you (potentially) see failing are because of
changes you made. Either of three things happen:

- You accidentally modified behavior you didn't mean to and
  introduced a bug you need to fix.
- Or, tests need to be modified because the intended behavior
  changed

The rest of the time today will be spent writing new tests.

---

## Open Issues

- Designing the fall semester's game

---

## End

Thanks for showing up. One small thing. I wrote down some
thoughts from reading articles about TDD and AI you can read
here if you're curious: `./06-addendum-AI-and-TDD.md`.

Happy Hacking!
