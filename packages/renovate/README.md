# Renovate

### We use Renovate Bot to keep our projects' dependencies up to date.

Add permissions for Renovate Bot to access your repository.

The file in this directory contains configuration for Renovate Bot,
allowing it to update dependencies while keeping SemVer constraints.

This means that if you add a dependency with version `^x.y.z`,
when Renovate Bot will open a PR to update that dependency,
it will do so with a `^` as well.
