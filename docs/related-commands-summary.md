# Related Commands Summary

## Command Explanations

### `git switch`

#### `git switch -c <branch-name>`: Create a new branch
- This command creates a new branch and switches to it immediately.
- Example: `git switch -c feature-xyz`

#### `git switch <branch-name>`: Switch to an existing branch
- This command switches to an existing branch.
- Example: `git switch dev`

### `git pull`

#### `git pull origin <branch-name>`: Pull the latest changes from a remote branch
- This command fetches and integrates changes from the specified remote branch.
- Example: `git pull origin dev`

### `git merge`

#### `git merge <source-branch>`: Merge changes from one branch to another
- This command merges changes from the source branch into the current branch.
- Example: `git merge feature-xyz`

### `git branch`

#### `git branch -d <branch-name>`: Delete a local branch
- This command deletes the specified local branch.
- Example: `git branch -d feature-xyz`

### `git push`

#### `git push origin --delete <branch-name>`: Delete a remote branch
- This command deletes the specified branch from the remote repository.
- Example: `git push origin --delete feature-xyz`

#### `git push origin <branch-name>`: Push changes to a remote branch
- This command pushes local changes to the specified remote branch.
- Example: `git push origin feature-xyz`

### `gh pr create`

#### `gh pr create --base <base-branch> --head <head-branch> --title "Pull Request Title" --body "Pull Request Description"`: Create a pull request (using GitHub CLI)
- This command creates a pull request on GitHub with the specified base and head branches, title, and description.
- Example: `gh pr create --base main --head feature-xyz --title "Add new feature" --body "This PR adds a new feature."`
