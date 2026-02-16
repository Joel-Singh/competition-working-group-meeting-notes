---
author: Joel Singh
---

# DU Code Competition Group
Welcome to the third meeting!

Take the first 5 minutes to introduce your name to a neighbor and make
some small talk. Additionally, download the zip I have put
on discord to one of the linux machines.

Additionally, here's todays programming fun fact:

The javascript deprecated `with` keyword:

```javascript
let a, x, y;
const r = 10;

with (Math) {
  a = PI * r * r;
  x = r * cos(PI);
  y = r * sin(PI / 2);
}

// As opposed to Math.PI, Math.cos, etc
```


---

## Today's Plan

- Learning basic git commands through an example of a
  templating system

- At next meeting, we'll use our beginning git knowledge
  to start modiifying the DU Slither code base! We'll each
  make a change and then combine all of those changes
  together with Git for a custom version.

---

## git init

The very first command you'll learn is `git init`, it,
initializes a git repo! I know crazy. Create a new
directory, copy the zip of initial files from the discord,
unzip it and open up the folder in a terminal. Then type:

`git init`

---

## git status

`git status` is your bread and butter. It lets you inspect
whats on the working tree and staging area as you work. If
you now type it after typing `git init`:

`git status`

you'll see some stuff about your files and how they
currently are not tracked.

---

## git add

`git add` adds your files to the staging area for being
eventually committed, it takes in files to be added, for
instance:

`git add src/index.html`

And then run:

`git status`

You can add all files at once with the -A option:

`git add -A`

And then, git status:

`git status`

---

## git commit

Now, to actually make a commit from all the files in your
staging area, you can use git commit! If you type:

`git commit`

Your editor will open up for you to type a message. For
now type something like "Initial commit" or along those
lines for your commit message.

---

## git log

Now, if you type `git log`, you can see the log of all
commits:

`git log`

You should see your first commit with the message you
typed! Now let's do some work...

---

## What Is Templating?

Templating is essentially a software layer over html.
Here, we will be implementing a very simple template
engine:

- It looks for strings within every html file in `src`
  that match `{header}` or `{footer}`, and then replaces
  that with our header or footer so that we don't need to
  manually type it on every page.

---

## git diff

Now, if we modify `template.py` to read in every html
file:

```python
file_names = ["./src/chips-and-salsa.html",
         "./src/enchiladas.html", "./src/index.html"]

file_contents = []

for file_name in file_names:
    with open(file_name, 'r') as file:
        content = file.read()
        file_contents.append((file_name, content))

print(file_contents)
```

We can then run `git diff`, to see all the changes we made
to the file. Then to commit we:

`git add template.py`
`git commit`

And finally, type `git log` to see your commit.

---

## Woops, we made a mistake!

We realize that we have the file names all pre-pended with
`./src`. To make it easier for when we save the modified
files in the directory `./out`, we'll refactor our code to
not do that:

```python
file_names = ["chips-and-salsa.html",
         "enchiladas.html", "index.html"]

file_contents = []

for file_name in file_names:
    with open("./src/" + file_name, 'r') as file:
        content = file.read()
        file_contents.append((file_name, content))

print(file_contents)
```

And now, we can `git diff`, `git add`, and `git commit`
for these changes.

---

## Implement templating

We do the workflow again to implement actually templating:

```python
for i in range(len(file_contents)):
    name, content = file_contents[i]
    content = content.replace("{header}", header)
    content = content.replace("{footer}", footer)
    file_contents[i] = (name, content)
```

`git diff`, `git add`, and `git commit`.

---

## Implement Writing Files

```python
for name, content in file_contents:
    with open("./out/" + name, "w") as file_object:
        file_object.write(content)
```

`git diff`, `git add`, and `git commit`.

Now running the program, you can open the files in a
browser to see the header and footers!

---

## git ignore

One thing you may have noticed, is that our `out`
directory is now "untracked" when we run `git status`. We
can tell Git to ignore it by adding a file called
`.gitignore` to the root of our directory containing file
paths we wish `git` to ignore:

In `./.gitignore`
`out`

The `.gitignore` itself is also version controlled. So
`git add` and `git commit` it to the repository.

---

## Pushing The Repository To Github

Click "new" on github. Fill out the name and description.
Copy the commands shown on the Github website to push what
you've done to Githug. we will go more in depth on these
in the future. And now, your repository is on Github!

---

## Reading For Next Time

Go through this Odin Project lesson:
https://www.theodinproject.com/lessons/foundations-git-basics
. One difference you'll notice is we created a local
repository on our machines and then put it on Github. In
the lesson, you'll create a repository on Github and then
clone it down to your local machine.

---

## End

- Next meeting will be Sunday, 7 to 8 pm once again
- As you have questions for the reading or practice,
  direct them to #competition-group-questions in discord.
  I'll be checking it regularly.

---

Happy Hacking!
