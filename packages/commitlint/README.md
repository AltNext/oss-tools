# CommitLint

### We use [`commitlint`](https://github.com/conventional-changelog/commitlint) in a [`commit-msg`](https://github.com/altnext/oss-tools/blob/main/packages/.husky/commit-msg) hook run by [`husky`](https://github.com/typicode/husky).

This configuration file is the most basic configuration needed in order to use `commitlint` and follow [`conventional-commits`](https://www.conventionalcommits.org) guidelines.

Add `@commitlint/cli`, `@commitlint/config-conventional` to your root `package.json`'s `devDependencies`.

See the [`.husky`](https://github.com/altnext/oss-tools/blob/main/packages/.husky) directory in this repository for instructions on how to automatically run `commitlint` on commit messages.

See the [`.github`](https://github.com/altnext/oss-tools/blob/main/packages/.github) directory in this repository for instructions on how to add a status check to verify PR titles,
according to the same `conventional-commits` guidelines.
