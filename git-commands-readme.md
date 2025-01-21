# Git Commands Reference Guide

## Basic Terminal Commands
- `ls`: List down data of current working directory
- `ls -a`: List down hidden repo also
- `pwd`: Path of current working directory
- `cd`: Change directory to given path
- `clear`: Clear the terminal
- `cd ..`: Go back one step
- `cd /`: Go back to the root directory
- `cd ~`: Go back to home directory
- `touch filename.type`: Create a file
- `touch filename1.type filename2.type`: Create multiple files
- `mkdir`: Create a new folder/repo
- `mkdir foldername1 foldername2`: Create multiple folders at once
- `rm filename.type`: Delete file
- `rmdir foldername`: Delete directory
- `rm -rf foldername`: Delete directory having data

## Git Configuration
```bash
git config --global user.name "My Name"
git config --global user.email "someone@email.com"
git config --list
```

## Repository Initialization and Remote Setup
```bash
# Initialize a new repository
git init

# Add remote origin
git remote add origin <link>

# Verify remote
git remote -v

# Check branch
git branch

# Rename branch
git branch -M main

# Push to main branch
git push origin main
```

## Basic Git Operations

### Adding & Committing
- Add files to staging area:
  ```bash
  git add <file name>
  ```
- Record changes:
  ```bash
  git commit -m "commit message"
  ```

### Merging Code
#### Way 1: Direct Merge
```bash
# Compare commits, branches, files & more
git diff <branch name>

# Merge two branches
git merge <branch name>
```

#### Way 2: Pull Request
Create a PR through your Git platform (e.g., GitHub, GitLab)

### Branch Operations
```bash
# Check current branch
git branch

# Rename branch
git branch -M main

# Navigate to branch
git checkout <branch name>

# Create new branch and switch to it
git checkout -b <new branch name>

# Delete branch
git branch -d <branch name>
```

### Undoing Changes
1. For staged changes:
   ```bash
   git reset <file name>
   git reset
   ```

2. For committed changes (one commit):
   ```bash
   git reset HEAD~1
   ```

3. For multiple commits:
   ```bash
   git reset <commit hash>
   git reset --hard <commit hash>
   ```

### Clone & Status
```bash
# Clone repository to local machine
git clone <some link>

# Check repository status
git status
```

### Push & Stash Operations
```bash
# Push to remote repository
git push origin main

# Save changes temporarily
git stash

# Apply stashed changes
git stash apply

# Clear stash
git stash clear
```

## Best Practices
1. Always pull before pushing changes
2. Write clear, descriptive commit messages
3. Create feature branches for new development
4. Keep commits atomic and focused
5. Regularly sync with the main branch
6. Use meaningful branch names
7. Review changes before committing

## Common Workflows
1. Feature Development:
   ```bash
   git checkout -b feature-branch
   # Make changes
   git add .
   git commit -m "Add feature"
   git push origin feature-branch
   # Create PR
   ```

2. Updating Local Repository:
   ```bash
   git pull origin main
   git checkout -b new-feature
   # Make changes
   ```

3. Resolving Conflicts:
   ```bash
   git pull origin main
   # Fix conflicts
   git add .
   git commit -m "Resolve conflicts"
   git push
   ```
