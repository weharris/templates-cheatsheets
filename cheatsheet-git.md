
# Cheatsheet for Git

- [Push changes to an existing repo](#push-changes-to-an-existing-repo)
- [Working with branches - create, change, and merge](#working-with-branches---create-change-and-merge)
- [Initialize and push a new repo](#initialize-and-push-a-new-repo)
- [Rebase basics](#rebase-basics)
- [Rebase workflow, typical](#rebase-workflow-typical)

## Push changes to an existing repo
[(Back to top)](#cheatsheet-for-git)

```bash
# Check status of modified files
git status

# Add specific files to staging (or use . for all files)
git add filename.md
# OR add all modified files:
git add .

# Create commit with descriptive message
git commit -m "Description of changes"

# Push to remote repository (use -u only on first push per branch)
git push

# If pushing a new branch for the first time:
git push -u origin branch-name
```

## Working with branches - create, change, and merge
[(Back to top)](#cheatsheet-for-git)
```bash
# Start from main branch and update it
git checkout main
git pull origin main

# Create and switch to new branch
git checkout -b feature-branch

# Make changes to files, then stage and commit
git add .
git commit -m "Add new feature"

# Push branch to remote (first time, -u sets upstream tracking)
git push -u origin feature-branch

# Continue working: make more changes, commit as needed
git add .
git commit -m "Fix bug in feature"
git push

# When ready to merge: switch back to main
git checkout main

# Pull latest changes from remote main
git pull origin main

# Merge feature branch into main
git merge feature-branch

# Push merged changes to remote main
git push origin main

# Delete local branch (optional, after merge)
git branch -d feature-branch

# Delete remote branch (optional, after merge)
git push origin --delete feature-branch
```

## Initialize and push a new repo
[(Back to top)](#cheatsheet-for-git)
```bash
# Initialize a new git repository
git init 

# Add all files to staging
git add . 

# Create initial commit + "comment" (-m designates message)
git commit -m "Initial commit" 

# Create a new repository on GitHub (via web interface)
# Add the remote repo (replace your-username and repo-name):
git remote add origin https://github.com/your-username/repo-name.git

# Rename branch to main
git branch -M main

# Push to GitHub (first time)
git push -u origin main
```

## Rebase basics
[(Back to top)](#cheatsheet-for-git)

```bash
# Rebase current branch onto main
git rebase main

# Interactive rebase (last 3 commits)
git rebase -i HEAD~3

# Continue rebase after resolving conflicts
git add .
git rebase --continue

# Abort rebase (undo everything)
git rebase --abort

# Push after rebase (rewrites history)
git push --force-with-lease origin branch-name
```

## Rebase workflow, typical
[(Back to top)](#cheatsheet-for-git)
```bash
# Update feature branch with latest main
git checkout feature-branch
git rebase main

# If conflicts: resolve, then:
git add .
git rebase --continue

# Push rebased branch
git push --force-with-lease origin feature-branch
```