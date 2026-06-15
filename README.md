# Git & GitHub Self Practice

Welcome! In this exercise, you will practice the basic Git and GitHub workflow using a tiny website project.

By the end of this exercise, you should understand:

- What Git is
- What GitHub is
- How to clone a repository
- How to make changes to a project
- How to save changes using `git add` and `git commit`
- How to upload changes using `git push`
- Why commits are important before using AI tools to edit code

---

## 1. Git vs GitHub

**Git** is a version control tool.  
It saves the history of your project and lets you go back to previous versions.

**GitHub** is a website where Git repositories can be stored online and shared with others.

A simple way to remember this:

```text
Git = the tool that tracks changes
GitHub = the website where repositories live online
```

A **commit** is like a save point in a game.

```text
Before risky change → commit
AI broke the code → restore from commit
```

---

## 2. Your mission

You are joining a tiny startup called **MoodChef AI**.

MoodChef AI is a very simple website that recommends food based on your mood.

Your job is to:

1. Fork this repository
2. Clone your fork to your computer
3. Make changes to the website
4. Save each meaningful change with a commit
5. Push your work back to GitHub

---

## 3. Step 1 — Fork this repository

Click the **Fork** button at the top-right of this GitHub page.

This creates your own copy of the repository on GitHub.

Important:

```text
Fork = copy on GitHub
Clone = copy from GitHub to your computer
```

---

## 4. Step 2 — Clone your fork

After forking, open your own fork on GitHub.

Click the green **Code** button and copy the repository URL.

Then run:

```bash
git clone YOUR_REPOSITORY_URL
```

For example:

```bash
git clone https://github.com/YOUR-USERNAME/git-github-self-practice.git
```

Enter the project folder:

```bash
cd git-github-self-practice
```

Open it in VS Code:

```bash
code .
```

---

## 5. Step 3 — Look at the project

The project contains:

```text
index.html
style.css
README.md
GIT_CHEATSHEET.md
```

Open `index.html` in your browser to see the website.

You can usually do this by double-clicking the file.

---

## 6. Step 4 — Check the Git status

Before making changes, run:

```bash
git status
```

This command asks Git:

```text
What changed in my project?
```

At this point, Git should probably say that there is nothing to commit.

---

## 7. Step 5 — Make your first change

Open `index.html`.

Find this line:

```html
<h1>MoodChef AI</h1>
```

Change it to a funny app name, for example:

```html
<h1>Snack Oracle 3000</h1>
```

Save the file.

Now run:

```bash
git status
```

You should see that `index.html` was modified.

---

## 8. Step 6 — Commit your first change

First, add the changed file:

```bash
git add index.html
```

Now create a commit:

```bash
git commit -m "Update app title"
```

What happened?

```text
git add    = choose changes for the next save point
git commit = create the save point
```

---

## 9. Step 7 — Push your change to GitHub

Now upload your commit to GitHub:

```bash
git push
```

Refresh your GitHub page and check that the change appears there.

Important:

```text
commit = save locally
push   = upload to GitHub
```

---

## 10. Step 8 — Make another change

Open `index.html`.

Add two new mood recommendations inside the list.

For example:

```html
<li>Confused → Sushi</li>
<li>Sleepy → Pasta</li>
```

Then run:

```bash
git status
git add index.html
git commit -m "Add new mood recommendations"
git push
```

---

## 11. Step 9 — Improve the design

Open `style.css`.

Change something small, for example:

- the background color
- the title color
- the spacing
- the font size

Then run:

```bash
git status
git add style.css
git commit -m "Improve page styling"
git push
```

---

## 12. Step 10 — Simulate an AI mistake

Now let’s simulate a common situation:

You asked an AI tool to improve your website, but it accidentally broke something.

Open `index.html` and delete this line:

```html
<link rel="stylesheet" href="style.css">
```

Save the file.

Open the website in the browser again.

What happened?

The page still exists, but the design is gone.

Now check Git:

```bash
git status
```

Git knows that `index.html` changed.

---

## 13. Step 11 — Restore the file

Because you committed your previous good version, you can restore the file:

```bash
git restore index.html
```

Open the website again.

The design should be back.

This is the main lesson:

```text
Git does not stop us from making mistakes.
Git makes mistakes easier to recover from.
```

---

## 14. Final reflection questions

Answer these questions:

1. What is the difference between Git and GitHub?
2. What does `git clone` do?
3. What does `git status` show?
4. What does `git add` do?
5. What does `git commit` do?
6. What does `git push` do?
7. Why is it important to commit before asking AI tools to make large changes?

---

## 15. Suggested commit messages

Good commit messages:

```text
Update app title
Add new mood recommendations
Improve page styling
Fix broken stylesheet link
Update README instructions
```

Less helpful commit messages:

```text
changes
final
fix
stuff
please work
```

A good commit message explains what changed.
