# 📚 **Module 8: GitHub Advanced Features**

---

## 🔖 **Continuous Integration / Continuous Deployment (CI/CD)**

### 📌 **Introduction to GitHub Actions**

**GitHub Actions** is a built-in feature that helps automate tasks such as testing, building, and deploying your code.

* Based on **workflows** written in YAML files.
* Runs automatically based on events (e.g., push, pull request).
* Saves time by automating repetitive tasks.

**Example triggers:**

* Run tests when someone pushes code.
* Deploy app when a pull request is merged.

---

### 📌 **Automating Workflows**

**Common use-cases:**

* **Build**: Compile your code when changes are made.
* **Test**: Run automated tests on every push.
* **Deploy**: Automatically publish to GitHub Pages, Heroku, Firebase, etc.

**Example: Simple GitHub Actions Workflow**

```yaml
# .github/workflows/nodejs.yml
name: Node.js CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    - name: Setup Node
      uses: actions/setup-node@v3
      with:
        node-version: '16'
    - run: npm install
    - run: npm test
```

This runs tests whenever code is pushed.

---

## 🔖 **GitHub Pages**

### 📌 **Hosting Static Websites and Documentation**

**GitHub Pages** allows you to host:

* Portfolios
* Documentation
* Static HTML websites (including Jekyll-based blogs)

**How to use GitHub Pages:**

1. Go to **Settings** of your repository.
2. Scroll to **"Pages"** section.
3. Choose a branch (usually `main`) and `/root` or `/docs` folder.
4. GitHub generates a public website at:

   ```
   https://your-username.github.io/repo-name/
   ```

**Tip:** You can even use Markdown in README or `docs/` folder to generate documentation pages!

---

## 🔖 **Security and Permissions**

### 📌 **Protecting Branches and Enforcing Policies**

You can protect important branches like `main` to prevent accidental changes.

**Common branch protection rules:**

* Require pull request reviews before merging
* Restrict who can push to the branch
* Require status checks (like passing tests)

**How to enable:**

* Go to repository **Settings → Branches**
* Click “Add rule” under “Branch protection rules”

---

### 📌 **Secure Handling of Sensitive Information**

Never upload passwords, API keys, or credentials to GitHub!

**Best practices:**

* Add secrets to **GitHub Secrets** under repo Settings for GitHub Actions.

* Use `.gitignore` to avoid pushing sensitive files:

  ```bash
  echo ".env" >> .gitignore
  ```

* Rotate exposed secrets immediately if accidentally committed.

---

## 📝 **Summary of Advanced GitHub Features**

| Feature                | Purpose                                    |
| ---------------------- | ------------------------------------------ |
| **GitHub Actions**     | Automate tasks like testing and deployment |
| **GitHub Pages**       | Host static websites from your repo        |
| **Branch Protection**  | Prevent unauthorized changes               |
| **Secrets & Security** | Keep API keys and sensitive data safe      |
