# Changesets

### We use [changesets](https://github.com/atlassian/changesets) to automate changelog generation and package publishing.

Add the [`config.json`](https://github.com/altnext/oss-tools/blob/main/packages/.changeset/config.json) file in this directory to your repository's `.changeset` dir.

Add `@changesets/changelog-github`, `@changesets/cli` to your root `package.json`'s `devDependencies`,
and add a `release` script that runs `changeset publish`,
and a `prerelease` script that runs `yarn build` if needed.

To automatically open PRs that generate changelogs and publish packages,
see the [`release.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/release.yml) file in the [`.github`](https://github.com/altnext/oss-tools/blob/main/packages/.github) directory in this repository.

To get comments on PRs, notifying you of the changesets in them or lack thereof,
add permissions to [`changeset-bot`](https://github.com/apps/changeset-bot) to access your repository.
