# Daily Development Routine

To ensure smooth development and integration, each engineer should follow these daily routines:

## Starting New Work

- Create a new branch for your bugfix or feature based on the `dev` or `dev-2` branch.

```sh
git switch dev
git pull origin dev
git switch -c feature-xxx
```

### Start of the Day

- Pull the latest changes from the `dev` or `dev-2` branch.

```sh
git switch dev
git pull origin dev
```

- Merge your feature or bugfix branch with the latest `dev` or `dev-2` branch.

```sh
git switch feature-xxx
git merge dev
```

### During Development

- Commit changes frequently with clear and concise commit messages.

```sh
git add .
git commit -m "Your clear and concise commit message"
```

- Push your changes to the remote repository regularly.

```sh
git push origin feature-xxx
```

### After Completing a Bugfix or Feature

- Ensure your branch is up-to-date with the latest `dev` or `dev-2` branch.

```sh
git switch dev
git pull origin dev
git switch feature-xxx
git merge dev
```

- Create a pull request for code review if your feature or bugfix is complete.
- After the pull request is merged, delete the feature or bugfix branch.

```sh
git branch -d feature-xxx
git push origin --delete feature-xxx
```

## Related Commands Summary

For detailed explanations of related commands, please refer to the [Related Commands Summary](related-commands-summary.md) page.

- [`git switch <branch-name>`: Switch to an existing branch](related-commands-summary.md#git-switch)
- [`git pull origin <branch-name>`: Pull the latest changes from a remote branch](related-commands-summary.md#git-pull)
- [`git merge <source-branch>`: Merge changes from one branch to another](related-commands-summary.md#git-merge)
- [`git add .`: Stage changes for commit](related-commands-summary.md#git-add)
- [`git commit -m "message"`: Commit changes with a message](related-commands-summary.md#git-commit)
- [`git push origin <branch-name>`: Push changes to a remote branch](related-commands-summary.md#git-push)
- [`git branch -d <branch-name>`: Delete a local branch](related-commands-summary.md#git-branch)
- [`git push origin --delete <branch-name>`: Delete a remote branch](related-commands-summary.md#git-push)
