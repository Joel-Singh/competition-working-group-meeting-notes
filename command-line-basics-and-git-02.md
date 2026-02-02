---
author: Joel Singh
---

# DU Code Competition Group
Welcome to the second meeting!

Take the first 5 minutes to introduce your name to a neighbor and make
some small talk.

Additionally, here's a programming fun fact:

"runtime", "run-time", and "run time" can have differing technical meanings:

- The amount of time execution takes
- The dependencies needed to run a software
- The moment when an activity takes place

The meaning is dependent on whatever particular style guide you use. See
https://bobrubbens.nl/post/my-opinion-on-spelling-runtime/ or how the google
developer style guide defines them:
https://developers.google.com/style/word-list#runtime

---

## Today's Plan

- Manipulating files from the terminal
- Git: The really really epic save button for your code

---

## `mkdir`: Switching Into Our Own Directory

`mkdir`, as you can probably tell, makes a directory.

1. Open the terminal
2. Type `mkdir commandline-practice`

Now, if you type `ls`, you should see your directory

3. Type `cd commandline-practice` to change directory

Now you should be inside of that directory! If you type `pwd` to print your
current working directory, you should see something along the lines of:

`/home/username/commandline-practice`

---

## `nano`: Command Line Editor

So, how do we create files from the command line? We can use nano!

1. Type `nano`
2. Now use your keyboard to type some text
3. Type ctrl-o to get a file name dialog
4. Type in a file name and press enter to save
5. Type ctrl-x to exit
6. Now use `cat`, which prints whatever file you give it, to see your file on the command line. Such as `cat mysupercoolfile.txt`

Note: for the controls on the bottom, `^` stands for "ctrl". 

---

## `rm`: Removing files

`rm` is able to remove files.

1. Type `ls` to confirm the file you made with `nano` is still there
2. Type `rm thefilename.txt` to remove that file
3. Now, type `ls` again to see that the file has been removed

Important, there is no trash can, so whatever you delete is just gone forever.

---

## Two more commands: `mv` and `cp`

Two more useful commands are `mv` and `cp`. They stand for **m**o**v**e and
**c**o**p**y. They're in the reading for this week and you'd be able to reference
it when you need them.

---

## Interlude: Options and Manpages

Every command takes options. For instance:

1. Open a terminal
2. `mkdir try-to-remove-me`
3. `rm try-to-remove-me`

Will give you the error:

`rm: cannot remove 'try-to-remove-me': Is a directory`

You have to type:

4. `rm --recursive try-to-remove-me`

To successfully remove the directory.

`--recursive` is an option, specifically the long form. You could have also
done `rm -r try-to-remove-me` for the exact same result. To see all the options
for a command, you can access its manual page with `man some-command`. E.g

1. `man rm`
2. Use the arrow keys to scroll or type "/" to search

The man pages are also available online: https://manpages.ubuntu.com/

---

## GIT!!! woo yay awesome

- Git is a really epic save button for your code, it lets you:

- Collaborate and manage dozens of changes from multiple people on one codebase
- Keep offline copies of code on your computer, and easily update
- Store the history of code changes. Such as inspecting a line to get a
  description from the person who changed it years ago.

The reason we have been going through command line basics is because `git` is a
command line tool.

---

## Git's Underlying Model

So how does Git do all of this fancy stuff? It uses:

- Branches
- Commits
- Working Directory
- Staging Area

---

### Commits:

Commits record each *change* that happens to a code. It also records meta-data
such as the author, time, and a description. They're called commits, because
you are "committing" yourself to a change.

### Staging Area:

Before being committed, all changes must be *added* to the Staging Area. And
then those changes are committed.

### Working Directory:

All the current changes that have not been added to the Staging Area are said
to be in the Working Directory. It is simply just, the current files.

---

### Branches And Commits Are Like Trees

Commits, each pointing to a previous commit, form a history of changes. The
current state of the code is built up by applying all the commits up to that
point.

A *branch* is a pointer to a specific commit. It is called a branch, because
having branches often forms a tree like structure. The commits multiple
branches point to often have a common ancestor. As if they're branching off
from it!

### Why All This?

Because all the commands you'll see and type regarding Git operate on this
conceptual model. They aren't _just_ arcane incantations, there is rhyme and
reason to them.

---

# Reading For Next Time

## Software Carpentry Article
- Read through https://swcarpentry.github.io/shell-novice/03-create.html (from the TOP lesson from last week)

## Command Line Practice
- Do the following practice (this is from https://www.theodinproject.com/lessons/foundations-command-line-basics)

Let’s practice creating files and directories and deleting them! You’ll need to enter the commands for the steps below in your terminal.

1. Create a new directory in your home directory with the name `test`.

2. Navigate to the `test` directory.

3. Create a new file called `test.txt`. Hint: use the touch _command_.

4. Open your newly created file in VSCode, make some changes, save the file, and close it.

5. Navigate back out of the `test` directory.

6. Delete the `test` directory.

That’s it—you’re done with practice! If you commit to doing most tasks from the command line from here on out, these commands will become second nature to you. Moving and copying files is much more efficiently done through the command line, even if it feels like more of a hassle at this point.

## Configuring Git And Github

There will be some configuration necessary to use Git with GitHub (which are two separate things!). Follow the steps outlined in https://www.theodinproject.com/lessons/foundations-setting-up-git .

GitHub is like google drive but for Git. These steps will essentially "log you
in" to GitHub from the command line. Letting you do things like use `git` on
the command line to upload commits. In the future, GitHub is the primary way
we'll share the code we make for the competitions.

---

# End

- Next meeting will be Sunday, 7 to 8 pm once again
- As you have questions for the reading or practice, direct them to #competition-group-questions in discord. I'll be checking it regularly.

Happy Hacking!
