
## Push changes to an existing repo

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

## Initialize and push a new repo
```bash
# Initialize a new git repository
git init 

# Add all files to staging
git add . 

# Create initial commit + "comment"
git commit -m "Initial commit" 

# Create a new repository on GitHub (via web interface)
# Add the remote repo (replace your-username and repo-name):
git remote add origin https://github.com/your-username/repo-name.git

# Rename branch to main
git branch -M main

# Push to GitHub (first time)
git push -u origin main
```

