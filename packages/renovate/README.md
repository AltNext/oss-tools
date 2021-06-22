# Renovate

### We use [Renovate Bot](https://github.com/renovatebot/renovate) to keep our projects' dependencies up to date.

Add permissions for [Renovate Bot](https://github.com/apps/renovate) to access your repository.

The [`renovate.json`](https://github.com/altnext/oss-tools/blob/main/packages/renovate/renovate.json) file in this directory contains configuration for Renovate Bot,
allowing it to update dependencies while keeping [SemVer](https://semver.org) constraints.

This means that if you add a dependency with version `^x.y.z`,
when Renovate Bot will open a PR to update that dependency,
it will do so with a `^` as well.
