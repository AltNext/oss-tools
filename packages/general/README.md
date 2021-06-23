## GitHub

### Settings

In [Options](https://github.com/AltNext/oss-tools/settings)., turn off the Wikis and Projects features, allow only squash merging, and automatically delete head branches.

In [Manage access](https://github.com/AltNext/oss-tools/settings/access), add our developers team as maintainers.

In [Security & analysis](https://github.com/AltNext/oss-tools/settings/security_analysis), enable Dependabot alerts.

In [Branches](https://github.com/AltNext/oss-tools/settings/branches), add branch protection for the `main` branch:
* Require pull request reviews before merging
    * Dismiss stale pull request approvals when new commits are pushed
* Require status checks to pass before merging
    * Require branches to be up to date before merging
    * Add any status checks you want to make required
* Require conversation resolution before merging
* Require linear history
* Include administrators

## NPM

### We use [`npm`](https://www.npmjs.com) to host our OSS libraries.

Add the [`package.json`](https://github.com/altnext/oss-tools/blob/main/packages/general/package.json) file from this directory to your project's root,
changing the [name](https://github.com/altnext/oss-tools/blob/main/packages/general/package.json#L2), [description](https://github.com/altnext/oss-tools/blob/main/packages/general/package.json#L4) and [`repository.url`](https://github.com/altnext/oss-tools/blob/main/packages/general/package.json#L14) as needed.

## Yarn

### We use [`yarn@1`](https://classic.yarnpkg.com) as our package manager.

Run `npm i -g yarn` to get the latest `yarn v1`.
To install dependencies in any project,
`cd` into it and run `yarn` at the command line.

## Code of conduct
We provide a standard code of conduct,
taken from [GitHub's recommended code of conduct](https://github.com/AltNext/oss-tools/community/code-of-conduct/new?template=contributor-covenant) for open source projects.

Place the [`CODE_OF_CONDUCT.md`](https://github.com/altnext/oss-tools/blob/main/packages/general/CODE_OF_CONDUCT.md) file from this directory in your repository's root,
changing the [contact e-mail](https://github.com/altnext/oss-tools/blob/main/packages/general/CODE_OF_CONDUCT.md#L63) if needed.

## Contributing
We provide a generic contributing guide, adapted from [@necolas](https://github.com/necolas)'s
[issue-guidelines](https://github.com/necolas/issue-guidelines).

Place the [`CONTRIBUTING.md`](https://github.com/altnext/oss-tools/blob/main/packages/general/CONTRIBUTIN.md) file from this directory in your repository's root,
replacing the placeholders with the specific repository settings and changing any steps necessary for CI to pass (tests, lint, ...).

## License
We use the MIT license for our open source projects.

Place the [`LICENSE`](https://github.com/altnext/oss-tools/blob/main/packages/general/LICENSE) file from this directory in your repository's root.
