# Related Commands Summary

## Command Explanations

### `git switch`

**`git switch -c <branch-name>`**: Create a new branch

- This command creates a new branch and switches to it immediately.
- Example:
    
```bash
git switch -c feature-xyz
```

**`git switch <branch-name>`**: Switch to an existing branch

- This command switches to an existing branch.
- Example:
    
```bash
git switch dev
```

### `git pull`

**`git pull origin <branch-name>`**: Pull the latest changes from a remote branch

- This command fetches and integrates changes from the specified remote branch.
- Example:
    
```bash
git pull origin dev
```

### `git merge`

**`git merge <source-branch>`**: Merge changes from one branch to another

- This command merges changes from the source branch into the current branch.
- Example:
    
```bash
git merge feature-xyz
```

### `git branch`

**`git branch -d <branch-name>`**: Delete a local branch

- This command deletes the specified local branch.
- Example:
    
```bash
git branch -d feature-xyz
```

### `git push`

**`git push origin --delete <branch-name>`**: Delete a remote branch

- This command deletes the specified branch from the remote repository.
- Example:
    
```bash
git push origin --delete feature-xyz
```

**`git push origin <branch-name>`**: Push changes to a remote branch

- This command pushes local changes to the specified remote branch.
- Example:

```bash
git push origin feature-xyz
```
