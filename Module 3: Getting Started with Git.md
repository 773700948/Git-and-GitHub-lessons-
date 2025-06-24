# 📚 **Module 3: Getting Started with Git**

---

## 🔖 **What is Git?**

### 📌 **Definition**

**Git** is a powerful, open-source distributed version control system designed to handle projects of all sizes efficiently. It tracks changes, coordinates work among multiple developers, and maintains a clear history of project evolution.

---

### 📌 **Key Features and Advantages**

* **Distributed System:**
  Every developer has the entire project's history locally, allowing offline work and faster operations.

* **Branching and Merging:**
  Git makes branching and merging easy and fast, supporting multiple parallel workflows.

* **Data Integrity:**
  Git ensures the integrity of your project by uniquely identifying and verifying each change.

* **High Performance:**
  Lightweight and efficient, suitable for both small projects and large codebases.

* **Open-source and Widely Adopted:**
  Large community support and excellent compatibility with tools like GitHub and GitLab.

---

### 📌 **Installation on Windows, Linux, and Mac**

**Windows:**

* Download Git from: [https://git-scm.com/download/win](https://git-scm.com/download/win)
* Run the installer, accepting default settings for simplicity.

---

## 🔖 **Git Configuration**

### 📌 **Setting User Identity (Name, Email)**

* After installation, configure your identity for commit tracking:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

*Verify settings with:*

```bash
git config --global --list
```

---

### 📌 **Basic Configurations (`git config`)**

* Set default text editor (e.g., VS Code, Vim):

```bash
git config --global core.editor "code --wait"
```

* Improve readability of Git outputs with colors:

```bash
git config --global color.ui auto
```

* Check current Git configuration:

```bash
git config --list
```

---

## 🔖 **Git Basics**

### 📌 **Creating Repositories**

* **New Repository (from scratch):**

```bash
git init my-project
cd my-project
```

* **Clone an Existing Repository:**

```bash
git clone https://github.com/user/repo.git
cd repo
```

---

### 📌 **Staging and Committing Changes**

* **Adding Changes (Staging):**

```bash
git add filename      # Stage specific file
git add .             # Stage all changes in directory
```

* **Committing Changes:**

```bash
git commit -m "Descriptive commit message"
```

*Example:*

```bash
git add index.html
git commit -m "Add homepage layout"
```

---

### 📌 **Viewing Commit History (`git log`)**

* To view detailed commit history:

```bash
git log
```

* To see a simplified, cleaner history:

```bash
git log --oneline
```

* View recent commits graphically:

```bash
git log --oneline --graph --decorate
```

---

## 📝 **Summary of Git Basic Commands**

| Command                   | Description                      |
| ------------------------- | -------------------------------- |
| `git init`                | Create a new repository locally  |
| `git clone [url]`         | Clone an existing repository     |
| `git add [file]`          | Stage changes for commit         |
| `git commit -m "message"` | Save staged changes with message |
| `git log`                 | Show commit history              |
| `git config --global`     | Set global Git configurations    |
