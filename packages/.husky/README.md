# Husky

### We use [`husky`](https://github.com/typicode/husky) to run tests, verify commit messages and generate docs before committing and pushing changes in our repositories.

Add `husky` to your root `package.json`'s `devDependencies`,
and add a `prepare` script that runs `husky install`.

After adding any of the following script,
run `yarn prepare` before committing anything,
for the scripts to register.

## [`commit-msg`](https://github.com/altnext/oss-tools/blob/main/packages/.husky/commit-msg)
Runs [`commitlint`](https://github.com/conventional-changelog/commitlint) on the commit message,
to verify it is written according to [`conventional-commits`](https://www.conventionalcommits.org) guidelines.

See the [`commitlint`](https://github.com/altnext/oss-tools/blob/main/packages/commitlint) directory in this repository for instructions on how to add `commitlint` to your repository.

## [`pre-commit`](https://github.com/altnext/oss-tools/blob/main/packages/.husky/pre-commit)
Runs [`typedoc`](https://github.com/TypeStrong/typedoc) to generate/update documentation files from TypeScript files and interfaces and JSDoc comments.
It also adds the changed files to your commit before it is made.

See the [`typescript`](https://github.com/altnext/oss-tools/blob/main/packages/typescript) directory in this repository for instructions on how to add `typedoc` to your projects.

## [`pre-push`](https://github.com/altnext/oss-tools/blob/main/packages/.husky/pre-push)
Tests your project before pushing changes to the remote.

See the [`jest`](https://github.com/altnext/oss-tools/blob/main/packages/jest) directory in this repository for instructions on how to add `jest` and tests to your projects.
