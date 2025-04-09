# 🧬 AI Lab – Team Collaboration Guide

Welcome to the team! This guide explains how to collaborate using Git + GitHub + VS Code or Jupyter Notebooks.

---

## 📦 Getting Started

### 1. Clone the repository
#### In VS Code:
- Open VS Code
- Press `Ctrl+Shift+P` → Type: `Git: Clone`
- Paste the repo URL: `https://github.com/katiarusso/AI-Project.git`
- Choose a folder (e.g. Desktop)
- Click **Yes** to open the repo
---

## 🔄 Daily Workflow

Always follow this cycle to keep the project clean and avoid conflicts:

### ✅ 1. Pull before working
```bash
git pull origin main
```
> 💡 This updates your local files with the latest version from GitHub.

### 📝 2. Work on your files
- Create or edit Jupyter notebooks in the `notebooks/` folder
- Use descriptive names

### 💾 3. Save, add, and commit your changes
```bash
git add .
git commit -m "Meaningful message (e.g. added PCA analysis for MCF7)"
```

### 🚀 4. Push to GitHub
```bash
git push origin main
```

---

## 🧠 Best Practices

- 📥 Always `git pull` before starting
- 📤 Always `git push` after finishing
- ❗ Only one person edits the **same file at the same time**
- 🧾 Write clear commit messages
  
---

## 🛠️ Optional commands

### See which files you’ve modified
```bash
git status
```

### Add a specific file
```bash
git add notebooks/my_analysis.ipynb
```

### Undo uncommitted changes
```bash
git checkout -- filename
```

Happy coding! 💻🧠🧬

