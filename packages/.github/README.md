# GitHub flows

This directory contains 3 workflows and 1 configuration file,
all to be placed inside the `.github` directory of the repo.

## `generated-files-bot.yml`
### We use Google's Generated Files Bot to track changes to generated files, or files relating to our CI process.

Add permissions for Google's Generated Files Bot to access the repository.
Add to this file any files that should not be changed by outside collaborators,
or files that should not be manually changed.

## Workflows

### `test.yml`
Generic JavaScript testing workflow.
Modify `jobs.test.strategy.matrix.node-version` to test against different NodeJS versions.

See this repository's `jest` directory for instructions on how to add `jest` to your project to test it.

### `codeql-analysis.yml`
Generic CodeQL analysis workflow.
Modify `jobs.analyze.strategy.matrix.language` to analyze languages other than {Java,Type}Script.

### `release.yml`
Generic JavaScript publishing workflow.

See this repository's `.changeset` directory for instructions on how to add `changesets` to your repository.
