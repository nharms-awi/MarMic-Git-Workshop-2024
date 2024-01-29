# Git Cheat sheet

## Local repository
- `git init`: Initialize a new git repository
- `git status`: Check the status of the current repository
- `git add <file>`: Stage a file for commit
  - `git add .`: Stage all changes in the current directory
- `git commit`: Create a new commit
  - `git commit --message "message"` : Commit changes with a commit message
- `git log`: View commit history
- `git diff`: View changes that have not been staged
  - `git diff --staged`: View changes that have been stage
- `git reset <file>`: Unstage a file
- `git checkout <file>`: Discard changes in a file
- `git switch <branch>`: Switch to the branch
  - `git switch --create <branch>`: Create a new branch and switch to it

## Branching and merging
- `git branch`: View all branches in the repository
- `git branch -d <branch>`: Delete a branch
- `git merge <branch>`: Merge changes from a branch into the current branch
- `git rebase <branch>`: Rebase the current branch onto another branch

## Remote repository
- `git clone <repo>`: Clone a remote repository
- `git fetch`: Download new commits from the remote repository
- `git pull`: Fetch and merge changes from a remote repository
- `git push <remote> <branch>`: Push commits to a remote repository
- `git remote add <remote> <repo>`: Add a new remote