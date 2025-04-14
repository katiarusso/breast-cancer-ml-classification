# 🧬 AI Lab – Team Collaboration Guide

Welcome to the team! This guide explains how to collaborate using Git + GitHub + VS Code or Jupyter Notebooks.

---

## 📦 Getting Started

### 1. Clone the repository
- Open VS Code
- Press `Ctrl+Shift+P` (per macOs: `Cmd+Shift+P`) → Type: `Git: Clone`
- Paste the repo URL: `https://github.com/katiarusso/AI-Project.git`
- Choose a folder where to clone the repo, possibly a new empty one (e.g. Desktop/AI-Project)
- Click **Yes** to open the repo

### 2. Import Data files
- Create a folder `Data` inside `AI-Project`
- Create the two folder `SmartSeq` and `DropSeq` inside `Data`
- Paste the data files inside

#### ⚠️ Note:
The folder name have to be exactly the ones I wrote, and they are case-sensitive, so the path in the code will work for everyone.

---

## 🔄 Daily Workflow

Always follow this cycle to keep the project clean and avoid conflicts:

### ✅ 1. Pull before working
```bash
git pull origin main
```
> 💡 This updates your local files with the latest version from GitHub.

### 📝 2. Work on your files
Each one of us will work on a notebook (task specific), in this way we will avoid conflicts with the main notebook `main.ipynb`.
- Create or edit your notebook in the `notebooks/` folder (e.g., `data_cleaning.ipynb`)

### 💾 3. Control check
- Save the changes (`Ctrl+S` or `Cmd+S`)

```bash
git status
```
> 💡 Check which files you have modified

You should see something like:
```bash
Changes not staged for commit:
  modified:   notebooks/data_cleaning.ipynb
```

### 💾 4. Add and commit the changes

```bash
git add notebooks/data_cleaning.ipynb
git commit -m "Meaningful message (e.g. added PCA analysis for MCF7)"
```

### 🚀 5. Push to GitHub
```bash
git push origin main
```
> 💡 This updates the repo with your changes.

---

### 🚨 In case you modified accidentally other files
You'll see something like:
```bash
git status
```

```bash
Changes not staged for commit:
  modified:   notebooks/data_cleaning.ipynb
  modified:   notebooks/data_visualization.ipynb
```
so after the push, add this step:
```bash
git restore notebooks/data_visualization.ipynb
```

---

## 🧠 Best Practices

- 📥 Always `git pull` before starting
- 📤 Always `git push` after finishing
- ❗ Only one person edits the **same file at the same time**
- 🧾 Write clear commit messages

