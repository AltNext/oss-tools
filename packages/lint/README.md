# Lint

### We use a dynamic, complex, constantly varying configuration to lint our code.

## [ESLint](https://github.com/eslint/eslint)

We maintain an open source `eslint` config, published at [`eslint-config-altnext`](https://github.com/altnext/eslint-config-altnext).

Add `eslint-config-altnext` to your project `package.json`'s `devDependencies`,
and add a `lint` script that runs `eslint --ext .ts,.tsx . --cache` (for example, for a project containing [React](https://github.com/facebook/react)).

If you want to run `lint-staged`,
add `lint-staged` to your root `package.json`'s `devDependencies` and add the following field:
```
  "lint-staged": {
    "**/*.{js,jsx,ts,tsx}": [
      "eslint --quiet --cache"
    ]
  }
```

Copy the [`.prettierrc.js`](https://github.com/altnext/oss-tools/blob/main/packages/lint/.prettierrc.js) file from this directory to the root of your project,
and the contents of either [`.eslintrc.js`](https://github.com/altnext/oss-tools/blob/main/packages/lint/.eslintrc.js) or [`.eslintrc.type-checking.js`](https://github.com/altnext/oss-tools/blob/main/packages/lint/.eslintrc.type-checking.js) into a `.eslintrc.js` file,
again in your project's root.

The [`husky`](https://github.com/altnext/oss-tools/blob/main/packages/.husky) directory here has instructions on how to add linting as a pre-commit hook,
while the [`.github`](https://github.com/altnext/oss-tools/blob/main/packages/.github) directory's [`test.yml`](https://github.com/altnext/oss-tools/blob/main/packages/.github/workflows/test.yml) workflow runs it as part of your CI.