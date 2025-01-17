# Git Branch Planning

## Scenario

In a project with multiple development phases and several team members, it is essential to maintain separate branches for different environments. This ensures that the first phase can be maintained while the second phase is being developed.

## Branches

- **prod**: Production environment code
- **stage**: Pre-release environment, ready for deployment
- **uat**: User Acceptance Testing environment
- **dev**: Development environment

## Second Phase Development

After the first phase goes live, the following branches are added to maintain the first phase and simultaneously develop the second phase features:

- **stage-2**
- **uat-2**
- **dev-2**

## Merging Changes

When bugs are fixed or new features are added in the first phase, the changes need to be merged from the `prod` branch to the `dev-2` branch of the second phase to ensure consistency and continuity in development.

## Branching Strategy for Team Members

Each team member should create a separate branch for modifying bugs or adding new features. The naming convention for these branches should be as follows:

- **feature-xxx**: For new features
- **bugfix-xxx**: For bug fixes

### Example Commands

To create a new feature branch:
```sh
git switch -c feature-xxx
```

To create a new bugfix branch:
```sh
git switch -c bugfix-xxx
```

Once the work is completed on these branches, they should be merged into the `dev` or `dev-2` branch, depending on the development phase.

To merge a feature or bugfix branch into `dev`:
```sh
git switch dev
git pull origin dev
git merge feature-xxx
git push origin dev
```

## Daily Development Routine

To ensure smooth development and integration, each engineer should follow these daily routines:

1. **Start of the Day**:
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

2. **During Development**:
   - Commit changes frequently with clear and concise commit messages.
   ```sh
   git add .
   git commit -m "Your clear and concise commit message"
   ```
   - Push your changes to the remote repository regularly.
   ```sh
   git push origin feature-xxx
   ```

3. **After Completing a Bugfix or Feature**:
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

- [`git switch -c <branch-name>`: Create a new branch](related-commands-summary.md#git-switch)
- [`git switch <branch-name>`: Switch to an existing branch](related-commands-summary.md#git-switch)
- [`git pull origin <branch-name>`: Pull the latest changes from a remote branch](related-commands-summary.md#git-pull)
- [`git merge <source-branch>`: Merge changes from one branch to another](related-commands-summary.md#git-merge)
- [`git branch -d <branch-name>`: Delete a local branch](related-commands-summary.md#git-branch)
- [`git push origin --delete <branch-name>`: Delete a remote branch](related-commands-summary.md#git-push)
- [`git push origin <branch-name>`: Push changes to a remote branch](related-commands-summary.md#git-push)
- [`gh pr create --base <base-branch> --head <head-branch> --title "Pull Request Title" --body "Pull Request Description"`: Create a pull request (using GitHub CLI)](related-commands-summary.md#gh-pr-create)
