# Jest

### We use [`jest`](https://github.com/facebook/jest) and [`ts-jest`](https://github.com/kulshekhar/ts-jest) to run tests on our TypeScript projects and collect coverage data

Add the [`jest.config.ts`](https://github.com/altnext/oss-tools/blob/main/packages/jest/jest.config.ts) file in this directory to your project's root.

Add `@types/jest`, `@jest/types`, `jest`, [`jest-junit`](https://github.com/jest-community/jest-junit), `ts-jest` to your project `package.json`'s `devDependencies`,
and add a `test` script that runs `jest --ci`.

Make sure to use `jest@>=27.0.0`, to be able to use a config file written in TypeScript.

See the [`typescript`](https://github.com/altnext/oss-tools/blob/main/packages/typescript) directory in this repository for instructions on how to add TypeScript to your project.
