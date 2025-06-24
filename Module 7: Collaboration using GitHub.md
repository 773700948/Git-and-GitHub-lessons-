# 📚 **Module 7: Collaboration using GitHub**

---

## 🔖 **Forking and Cloning**

### 📌 **Forking Repositories**

A **fork** is your personal copy of someone else's GitHub repository, allowing you to freely experiment and make changes without affecting the original.

**How to Fork:**

* Visit the repository on GitHub.
* Click the **"Fork"** button (top-right corner).
* GitHub creates a personal copy under your account.

---

### 📌 **Cloning Forks and Upstream Synchronization**

**Cloning** downloads a copy of your repository to your local computer.

**Clone your fork:**

```bash
git clone https://github.com/your-username/repository-name.git
cd repository-name
```

**Setting upstream (original repository):**

```bash
git remote add upstream https://github.com/original-author/repository-name.git
```

**Syncing your fork with upstream:**

```bash
git fetch upstream
git merge upstream/main  # or the main branch name (master/main)
git push origin main
```

---

## 🔖 **Pull Requests (PRs)**

Pull Requests enable you to request others to review your changes before integrating (merging) them.

### 📌 **Creating and Managing PRs**

**How to create a PR:**

* Push changes to your forked repository.
* On GitHub, navigate to your fork and click **"Compare & pull request"**.
* Provide a clear title and description explaining your changes.
* Click **"Create Pull Request"**.

---

### 📌 **Code Reviews and Approval Workflows**

* Collaborators review the code in the PR, providing feedback through comments or suggesting changes.
* You can commit additional changes to the same PR to address the feedback.
* Once approved, the PR is merged into the main branch by repository maintainers.

**Typical PR Workflow:**

1. Create PR.
2. Code review (comments, suggestions).
3. Address feedback and update PR.
4. Approval.
5. Merge PR.

---

## 🔖 **Issues and Project Management**

GitHub issues are a powerful way to manage tasks, bugs, and improvements collaboratively.

### 📌 **Creating, Assigning, and Tracking Issues**

**Creating an issue:**

* Navigate to the "Issues" tab in your repository.
* Click **"New issue"**, provide a clear title, description, and click **"Submit"**.

**Assigning issues:**

* On an issue page, assign it to yourself or team members.

**Tracking issues:**

* Issues can be tracked through built-in filtering, status (open/closed), and linked to PRs.

---

### 📌 **Labels, Milestones, and GitHub Projects Board**

* **Labels:** Categorize and prioritize issues (e.g., `bug`, `feature`, `high-priority`).
* **Milestones:** Group issues toward specific project goals or deadlines.
* **Project Boards:** Visually organize issues, tasks, and PRs.

**Example workflow:**

* Issue created ➜ Assigned ➜ Labeled (priority/type) ➜ Added to milestone ➜ Tracked via project board.

---

## 📝 **Summary of GitHub Collaboration Commands & Terms**

| Term/Command                     | Description                                |
| -------------------------------- | ------------------------------------------ |
| **Fork**                         | Copy a repository under your account       |
| `git clone [url]`                | Clone repository to local computer         |
| `git remote add upstream [url]`  | Link original repository                   |
| **Pull Request (PR)**            | Propose and discuss changes before merging |
| **Issues**                       | Track tasks, bugs, and features            |
| **Labels, Milestones, Projects** | Organize tasks/issues visually             |
