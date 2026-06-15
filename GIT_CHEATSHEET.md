# Git & GitHub Cheat Sheet

## Basic ideas

```text
Git = version control tool
GitHub = website for hosting Git repositories
Repository / repo = project folder tracked by Git
Commit = save point
Clone = download a repo from GitHub to your computer
Push = upload your commits to GitHub
```

---

## Common commands

### Check what changed

```bash
git status
```

Use this often.

---

### Add changes to the next commit

Add one file:

```bash
git add index.html
```

Add all changed files:

```bash
git add .
```

---

### Create a commit

```bash
git commit -m "Write a clear message here"
```

Example:

```bash
git commit -m "Add new mood recommendations"
```

---

### Push commits to GitHub

```bash
git push
```

---

### Clone a repository

```bash
git clone REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/username/repository-name.git
```

---

### Restore a file to the last committed version

```bash
git restore index.html
```

Restore all changed files:

```bash
git restore .
```

Be careful: this deletes uncommitted changes.

---

## The basic workflow

```text
change files
→ git status
→ git add
→ git commit
→ git push
```

---

## Good commit messages

Good:

```text
Update app title
Add new recommendations
Improve page styling
Fix stylesheet link
```

Not so good:

```text
stuff
fix
final
changes
```

A good commit message answers:

```text
What changed?
```
