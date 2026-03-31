## Git & Github (Git Commands)

### 1. Setup & Config

```bash
git config --global user.name "Your Name"        # Set your Git username
git config --global user.email "you@email.com"   # Set your Git email
git config --list                                # Show all Git configs
git config --global core.editor "code --wait"    # Set default editor
```

### 2. Initialize & Clone

```bash
git init                      # Initialize a new Git repository
git clone <repo-url>          # Clone a remote repository
git clone -b <branch> <url>   # Clone a specific branch
```

### 3. Check Status & Info

```bash
git status                    # Show current changes (staged/unstaged)
git log                       # Show full commit history
git log --oneline             # Show compact commit history
git log --graph --oneline     # Visual commit graph
git show <commit-id>          # Show details of a commit
```

### 4. Staging & Commit

```bash
git add <file>                # Stage a specific file
git add .                     # Stage all changes
git commit -m "message"       # Commit staged changes
git commit -am "message"      # Stage + commit (tracked files only)
```

### 5. Compare Changes

```bash
git diff                      # Show unstaged changes
git diff --staged             # Show staged changes
git diff <branch1>..<branch2> # Compare two branches
```

### 6. Branching

```bash
git branch                    # List branches
git branch <name>             # Create new branch
git switch <branch>           # Switch to branch
git switch -c <name>          # Create + switch branch
git checkout <branch>         # Old way to switch branch
git checkout -b <name>        # Old way create + switch
```

### 7. Merge & Rebase

```bash
git merge <branch>            # Merge branch into current branch
git rebase <branch>           # Reapply commits on top of another branch
git rebase -i HEAD~3          # Interactive rebase (edit last 3 commits)
```

### 8. Remote (GitHub etc.)

```bash
git remote                    # List remote names
git remote -v                 # Show remote URLs
git remote add origin <url>   # Add remote repository
git remote remove origin      # Remove remote
git remote rename old new     # Rename remote

git remote set-url origin <url>     # Change remote URL
git remote set-url --add origin <url>   # Add another URL to remote
git remote set-url --delete origin <url> # Remove specific URL

git fetch                     # Fetch changes from remote
git fetch origin              # Fetch from specific remote
git fetch --all               # Fetch all remotes

git pull origin main          # Fetch + merge from remote branch
git push origin main          # Push to remote branch
git push -u origin main       # Push and set upstream
```

### 9. Undo & Reset

```bash
git restore <file>            # Discard changes in file
git restore --staged <file>   # Unstage file

git reset HEAD <file>         # Unstage file (older way)
git reset --soft HEAD~1       # Undo commit (keep changes)
git reset --hard HEAD         # Reset everything (danger)

git revert <commit-id>        # Undo commit safely (creates new commit)
```

### 10. Stash (Temporary Save)

```bash
git stash                     # Save changes temporarily
git stash list                # List stashes
git stash apply               # Apply stash
git stash pop                 # Apply + remove stash
git stash drop                # Delete stash
```

### 11. Tags

```bash
git tag                       # List tags
git tag v1.0                  # Create lightweight tag
git tag -a v1.0 -m "msg"      # Create annotated tag
git push origin v1.0          # Push tag
```

### 12. Search & Inspect

```bash
git grep "text"               # Search text in repo
git log --grep="msg"          # Search commit messages
git blame <file>              # Show who changed each line
git reflog                    # Show all HEAD movements
```

### 13. Advanced

```bash
git cherry-pick <commit-id>   # Apply commit from another branch
git bisect                    # Find buggy commit
```

### 14. Clean Up

```bash
git clean -f                  # Remove untracked files
git clean -fd                 # Remove files + directories
```

### 15. Submodules

```bash
git submodule add <repo>                # Add submodule
git submodule update --init --recursive # Initialize submodules
```

## MOST IMPORTANT (Must Remember)

If you remember just these, you’re become productive:

```bash
git clone <url>               # Get repo
git status                    # Check changes
git add .                     # Stage changes
git commit -m "msg"           # Save changes
git pull                      # Get latest updates
git push                      # Upload changes
git switch -c feature         # New branch
git merge feature             # Merge branch
git log --oneline             # View history
```
