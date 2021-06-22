# GitHub flows

This directory contains 3 workflows and 1 configuration file,
all to be placed inside the `.github` directory of the repo.

## [`generated-files-bot.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/generated-files-bot.yml)
### We use [Generated Files Bot](https://github.com/apps/generated-files-bot) to track changes to generated files, or files relating to our CI process.

Add permissions for Generated Files Bot to access the repository.

Add to this file any files that should not be changed by outside collaborators,
or files that should not be manually changed.

## Workflows

## [`test.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/test.yml)
Generic JavaScript testing workflow.
Modify [`jobs.test.strategy.matrix.node-version`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/test.yml#L15) to test against different NodeJS versions.

You can also remove steps that are not relevant to your project,
like `Type`, `Lint` or the `Coverage` steps.

Add the test run and coverage statuses to your protected branch's required status checks.

See this repository's [`jest`](https://github.com/altnext/oss-tools/blob/main/packages/jest) directory for instructions on how to add [`jest`](https://github.com/facebook/jest) to your project to run tests.

See this repository's [`lint`](https://github.com/altnext/oss-tools/blob/main/packages/lint) directory for instructions on how to add [`eslint`](https://github.com/eslint/eslint) to your project to lint your files.

See this repository's [`typescript`](https://github.com/altnext/oss-tools/blob/main/packages/typescript) directory for instructions on how to add [`typescript`](https://github.com/microsoft/TypeScript) to your project to add type safety.

## [`codeql-analysis.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/codeql-analysis.yml)
Generic CodeQL analysis workflow.
Modify [`jobs.analyze.strategy.matrix.language`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/codeql-analysis.yml#L23) to analyze languages other than {Java,Type}Script.

Add the analysis statuses to your protected branch's required status checks.

## [`release.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/release.yml)
Generic JavaScript publishing workflow.

See this repository's [`.changeset`](https://github.com/altnext/oss-tools/blob/main/packages/.changeset) directory for instructions on how to add [`changesets`](https://github.com/atlassian/changesets) to your repository.

## GitHub templates
We provide two generic issue templates and one generic pull request template.
To use them, simply place the [`ISSUE_TEMPLATE`](https://github.com/altnext/oss-tools/blob/main/packages/.github/ISSUE_TEMPLATE) directory and [`PULL_REQUEST_TEMPLATE.md`](https://github.com/altnext/oss-tools/blob/main/packages/.github/PULL_REQUEST_TEMPLATE.md) file in this repository inside your repository's `.github` directory.

## GitHub applications

### Do Not Merge GCF
We use this bot to block PRs with the label `do not merge` (or `do-not-merge`) from being merged.

Add permissions for this bot to access your repository to enable it.
