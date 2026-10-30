# Git command history

Commands run in `exam-project` for the local assessment work:

```sh
git init
git add .
git commit -m "Initial commit: setup project structure"
git branch -M main
git checkout -b feature-header
git add index.html
git commit -m "Add header component to index.html"
git checkout main
git merge --no-ff feature-header -m "Merge feature-header into main"
git checkout -b nav-feature
git add index.html
git commit -m "Add primary navigation menu"
git checkout main
git checkout -b nav-alt
git add index.html
git commit -m "Add alternative navigation menu"
git checkout main
git merge nav-feature
git merge nav-alt
git add index.html
git commit -m "Resolve merge conflict between nav-feature and nav-alt"
git remote add origin https://github.com/G1oka/exam-project.git
git push --all -u origin
```

Collaboration pull demonstration, using a second clone:

```sh
git clone /Users/giorgi/Documents/gadabareba/exam/exam-project /tmp/exam-project-collab
git remote set-url origin https://github.com/G1oka/exam-project.git
git add README.md COMMANDS.md
git commit -m "Document remote collaboration update"
git push origin main
# In the original checkout:
git pull origin main
```
