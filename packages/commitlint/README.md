# CommitLint

### We use `commitlint` in a `commit-msg` hook run by `husky`.

This configuration file is the most basic configuration needed in order to use `commitlint` and follow `conventional-commits` guidelines.

Add `@commitlint/cli`, `@commitlint/config-conventional` to your root `package.json`'s `devDependencies`.

See the `.husky` directory in this repository for instructions on how to automatically run `commitlint` on commit messages.

To add a status check to verify PR titles, according to the same `conventional-commits` guidelines.
