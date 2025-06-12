# Cloud-Computing-Learning

# 📘 Git and GitHub Workflow

This assignment will guide you through essential Git and GitHub operations including creating repositories, working with branches, performing merges, and forking projects.

---

## 🔹 Step 1: Initialize Local Repository
```bash
mkdir my-git-repo
cd my-git-repo
git init
echo "Initial project code" > index.html
git add .
git commit -m "Initial commit"
```

---

## 🔹 Step 2: Connect to Remote and Push
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```
> 💡 After pushing, add a new file like `README.md` manually on GitHub and then:
```bash
git pull origin main
```

---

## 🔹 Step 3: Create Branch `g1`, Add File, Raise Pull Request
```bash
git checkout -b g1
echo "This is a new file in g1" > g1_notes.txt
git add g1_notes.txt
git commit -m "Add g1_notes.txt"
git push origin g1
```
➡️ Now go to GitHub:
- Create a **Pull Request** from `g1` to `main`
- Merge the PR without conflicts

---

## 🔹 Step 4: Update Local Repo, Reset, and List Changes
```bash
git pull origin main
git status
git diff

# Reset last commit while keeping files
git reset --soft HEAD~1

# Reset and discard last commit
git reset --hard HEAD~1
```

---

## 🔹 Step 5: Create and Update Local Branches
```bash
git checkout -b b1
echo "B1 updates" > b1.txt
git add b1.txt
git commit -m "B1 changes"

git checkout -b b2
echo "B2 updates" > b2.txt
git add b2.txt
git commit -m "B2 changes"

git checkout -b b3
echo "B3 updates" > b3.txt
git add b3.txt
git commit -m "B3 changes"
```

---

## 🔹 Step 6: List Changes
```bash
# View differences between branches
git diff b1 b2
git diff b2 b3

# View file list
ls
```

---

## 🔹 Step 7: Local Merge and Delete Branches
```bash
git checkout main
git merge b1

git branch -d b1              # Delete local branch
git push origin --delete b1   # Delete remote branch
```

---

## 🔹 Step 8: Fork Repository
1. Go to GitHub and open the repository
2. Click **Fork** (top-right corner)
3. GitHub will create a copy under your username

```bash
# Clone the forked repo to your machine
git clone https://github.com/YOUR_USERNAME/FORKED_REPO.git
cd FORKED_REPO
```

---

✅ **End of Assignment**  
Feel free to explore more operations like rebasing, cherry-picking, and stash for advanced practice!
