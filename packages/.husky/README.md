# Husky

### We use `husky` to run tests, verify commit messages and generate docs before committing and pushing changes in our repositories.

Add `husky` to your root `package.json`'s `devDependencies`,
and add a `prepare` script that runs `husky install`.

After adding any of the following script,
run `yarn prepare` before committing anything,
for the scripts to register.

## `commit-msg`
Runs `commitlint` on the commit message,
to verify it is written according to `conventional-commits` guidelines.

See the `commitlint` directory in this repository for instructions on how to add `commitlint` to your repository.

## pre-commit
Runs `typedoc` to generate/update documentation files from TypeScript files and interfaces and JSDoc comments.
It also adds the changed files to your commit before it is made.

See the `typescript` directory in this repository for instructions on how to add `typedoc` to your projects.

## pre-push
Tests your project before pushing changes to the remote.

See the `jest` directory in this repository for instructions on how to add `jest` and tests to your projects.
