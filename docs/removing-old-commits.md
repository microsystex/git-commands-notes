# Removing Old Commits

When a repository has too many commits over a long period, you may need to remove commits older than six months. The following commands can help you achieve this:

## Commands

### Create a new branch

- Example:

```bash
git switch -c new-branch-name specific-commit-hash
```

### Reset to root commit

- Example:

```bash
git reset --soft root-commit-hash
```

### Amend commit message

- Example:

```bash
git commit --amend -m "Remove historical data, reduced to a single commit"
```

### Rebase onto temp branch

- Example:

```bash
git rebase specific-commit-hash main --onto temp-branch
```

### Delete temp branch

- Example:

```bash
git branch -d temp-branch
```

### Force push changes

- Example:

```bash
git push --force
```

## Related Commands Summary

For detailed explanations of related commands, please refer to the [Related Commands Summary](related-commands-summary.md) page.

- [`git switch -c <new_branch_name> <specific_commit_hash>`: Create a new branch from a specific commit](related-commands-summary.md#git-switch)
- [`git reset --soft <root_commit_hash>`: Reset the current branch to the root commit, keeping changes staged](related-commands-summary.md#git-reset)
- [`git commit --amend -m "Remove historical data, reduced to a single commit"`: Amend the current commit with a new message](related-commands-summary.md#git-commit)
- [`git rebase <specific_commit_hash> main --onto temp-branch`: Rebase the main branch onto a temporary branch starting from a specific commit](related-commands-summary.md#git-rebase)
- [`git branch -d temp-branch`: Delete the temporary branch](related-commands-summary.md#git-branch)
- [`git push --force`: Force push the changes to the remote repository](related-commands-summary.md#git-push)
