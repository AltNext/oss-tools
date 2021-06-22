# TypeScript

### We use [TypeScript](https://github.com/microsoft/TypeScript) as a primary language.

When creating a new JavaScript project,
copy the [`tsconfig.json`](https://github.com/altnext/oss-tools/blob/main/packages/typescript/tsconfig.json) file from this directory to use in your repository.

This file contains basic configuration to build TypeScript projects,
while ignoring test suites and transpiled files.

Add `typescript`, [`ts-node`](https://github.com/TypeStrong/ts-node) to your root `package.json`'s `devDependencies`,
and add a `build` script that runs `tsc`,
a `clean` script that runs `tsc --build --clean` and a `type` script that runs `tsc --noEmit --noImplicitAny`,
to each project that is going to be written in TypeScript.

## TypeDoc

### We use [`typedoc`](https://github.com/TypeStrong/typedoc) to automatically generate API documentation.
To add this capability to your repository,
add `typedoc`, [`typedoc-plugin-markdown`](https://github.com/tgreyuk/typedoc-plugin-markdown) to your project `package.json`'s `devDependencies`,
and add a `docs` script that runs `yarn typedoc --disableSources index.ts`.

Note the `--disableSources` is there to stop `typedoc` from linking to other files in the specific commit,
making the changes be solely documentation changes.
