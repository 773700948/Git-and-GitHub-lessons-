# 📚 **Module 4: Git Branching and Merging**

---

## 🔖 **Branching**

### 📌 **What is Branching?**

* **Branches** let you create separate lines of development within the same repository.
* Allows you to:

  * Experiment safely
  * Develop features independently
  * Work collaboratively without interference

---

### 📌 **Creating and Managing Branches**

* **Create a new branch:**

```bash
git branch branch_name
```

* **Switch to a branch:**

```bash
git checkout branch_name
```

*(Alternatively, newer Git version)*:

```bash
git switch branch_name
```

* **Create and switch immediately:**

```bash
git checkout -b branch_name
# or newer Git version:
git switch -c branch_name
```

* **View branches:**

```bash
git branch        # List all branches; current branch marked with *
git branch -a     # Include remote branches
```

* **Rename a branch:**

```bash
git branch -m old_branch new_branch
```

* **Delete a branch:**

```bash
git branch -d branch_name      # Delete merged branch
git branch -D branch_name      # Force delete unmerged branch
```

---

## 🔖 **Merging**

### 📌 **Combining Branches (Merge)**

* **Merge** integrates changes from one branch into another (e.g., merging a feature branch into main).

**Typical merge scenario:**

```bash
git checkout main           # Switch to main branch
git merge feature_branch    # Merge feature_branch into main
```

---

### 📌 **Resolving Merge Conflicts (Step-by-Step)**

When two branches modify the same file differently, **conflicts** occur:

**Step-by-Step Resolution:**

1. **Identify conflicts:**

```bash
git merge branch_name
```

* Git will indicate conflicts clearly.

2. **Open files** marked with conflicts (look for conflict markers):

```
<<<<<<< HEAD
Your changes (branch you're merging into)
=======
Incoming changes (branch you're merging from)
>>>>>>> branch_name
```

3. **Edit files** manually to resolve conflicts, choosing correct code lines.

4. **Stage fixed files**:

```bash
git add filename
```

5. **Complete merge with commit**:

```bash
git commit -m "Resolved merge conflict in file X"
```

---

## 🔖 **Advanced Merging Techniques**

### 📌 **Rebasing (`git rebase`)**

* **Rebase** reapplies commits from one branch onto another, creating a cleaner, linear history.

**Basic syntax:**

```bash
git checkout feature_branch
git rebase main
```

* This moves the commits from your `feature_branch` onto the latest commit of `main`.

---

### 📌 **Rebase vs. Merge: When to Use?**

| **Feature**   | **Merge**                                         | **Rebase**                                                           |
| ------------- | ------------------------------------------------- | -------------------------------------------------------------------- |
| History       | Preserves branching history clearly (non-linear). | Creates linear history (cleaner look).                               |
| Conflicts     | Resolved once, at merge time.                     | May need to resolve multiple times if rebasing commits individually. |
| Collaboration | Good for public/shared branches.                  | Prefer for private branches or before PRs.                           |

* **Recommended practice:**

  * **Merge** for public branches and collaborative workflows.
  * **Rebase** for local/private branches and maintaining a clean, linear history.

---

## 📝 **Summary of Branching and Merging Commands**

| Command                       | Description                            |
| ----------------------------- | -------------------------------------- |
| `git branch branch_name`      | Create a new branch                    |
| `git checkout branch_name`    | Switch to an existing branch           |
| `git checkout -b branch_name` | Create and immediately switch branches |
| `git merge branch_name`       | Merge branch into the current branch   |
| `git rebase branch_name`      | Reapply current branch on another      |
