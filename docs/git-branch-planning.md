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
