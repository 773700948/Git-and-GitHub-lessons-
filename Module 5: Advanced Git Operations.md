# 📚 **Module 5: Advanced Git Operations**

---

## 🔖 **Undoing Changes**

Git provides powerful ways to revert or undo changes to your project safely.

### 📌 **Reverting Commits (`git revert`)**

* Creates a new commit that undoes the changes made by a previous commit.
* Safe way to undo changes without erasing history.

**Usage:**

```bash
git revert <commit_hash>
```

**Example:**

```bash
git revert a1b2c3d4   # creates a new commit undoing changes made by commit a1b2c3d4
```

---

### 📌 **Resetting to Previous States (`git reset`)**

* Moves your branch backward to a specific commit.
* Three modes:

  * `--soft`: Keeps changes staged.
  * `--mixed` (default): Unstages changes, keeps them in working directory.
  * `--hard`: Completely discards changes.

**Usage examples:**

```bash
git reset --soft <commit_hash>   # Reset, keeping changes staged
git reset <commit_hash>          # Default: unstaged but changes remain
git reset --hard <commit_hash>   # Reset completely, discards changes
```

**Example:**

```bash
git reset --hard HEAD~1  # Removes latest commit and all changes permanently
```

---

## 🔖 **Working with Remote Repositories**

Remote repositories help teams collaborate and synchronize work effectively.

### 📌 **Setting Remote Repositories (`git remote`)**

* Add a new remote repository:

```bash
git remote add origin https://github.com/user/repo.git
```

* List remote repositories:

```bash
git remote -v
```

* Remove remote repository:

```bash
git remote remove origin
```

---

### 📌 **Synchronizing Changes**

* **Fetching (`git fetch`):** Download latest commits and branches from remote without merging:

```bash
git fetch origin
```

* **Pulling (`git pull`):** Fetch and merge changes from remote repository:

```bash
git pull origin main
```

* **Pushing (`git push`):** Upload local commits to remote repository:

```bash
git push origin main
```

---

## 🔖 **Stashing**

### 📌 **Temporarily Saving Changes (`git stash`)**

* Useful when switching branches or pausing current work without committing.

* Save changes temporarily:

```bash
git stash
```

* Save stash with a message:

```bash
git stash push -m "Message describing stash"
```

---

### 📌 **Retrieving Stashed Changes**

* Apply and remove the most recent stash:

```bash
git stash pop
```

* Apply a stash without removing:

```bash
git stash apply
```

* List all stashed changes:

```bash
git stash list
```

* Apply a specific stash:

```bash
git stash apply stash@{1}
```

* Remove specific stash:

```bash
git stash drop stash@{1}
```

---

## 📝 **Summary of Advanced Git Commands**

| Command                       | Description                               |
| ----------------------------- | ----------------------------------------- |
| `git revert <commit_hash>`    | Create new commit undoing previous commit |
| `git reset --soft <commit>`   | Reset commit but keep changes staged      |
| `git reset <commit>`          | Reset commit unstaged                     |
| `git reset --hard <commit>`   | Reset commit discarding changes           |
| `git remote add origin <url>` | Add remote repository                     |
| `git fetch origin`            | Fetch changes from remote                 |
| `git pull origin main`        | Pull (fetch and merge) from remote        |
| `git push origin main`        | Push changes to remote                    |
| `git stash`                   | Temporarily save changes                  |
| `git stash pop`               | Retrieve last stash                       |
| `git stash list`              | List all stashes                          |
