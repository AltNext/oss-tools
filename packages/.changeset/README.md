# Changesets

### We use changesets to automate changelog generation and package publishing.

Add the `config.json` file in this directory to your repository's `.changeset` dir.

Add `@changesets/changelog-github`, `@changesets/cli` to your root `package.json`'s `devDependencies`,
and add a `release` script that runs `changeset publish`,
and a `prerelease` script that runs `yarn build` if needed.

To automatically open PRs that generate changelogs and publish packages,
see the `release.yml` file in the `.github` directory in this repository.
