# Contributing

## Issues

You can find our open issues in the project's [issue tracker](https://github.com/vizzuhq/vizzu-ext-js-story/issues). Please let us know if you find any issues or have any feature requests there.

## Contributing

If you want to contribute to the project, your help is very welcome. Just fork the project, make your changes and send us a pull request.
You can find the detailed description of how to do this in
[Github's guide to contributing to projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects).

## CI-CD

### Development environment

You can initialize the development environment of vizzu-story with npm.

Run `npm install` or `npm update --dev` command to set up your environment.

```sh
npm install  # npm update --dev
```

**Note:** You can set up git hooks into your local git repository with the `prepare` script. Pre-commit hook is going to format the code with `prettier` and pre-push hook is going to run the CI steps.

```sh
npm run prepare
```

### CI

The CI steps check code formatting, run code analyses and run unit tests over the vizzu-story project.

The `check` script runs the above tasks.

```sh
npm run check
```

#### Formatting

The vizzu-story project is formatted with `prettier`.

Run the `prettier` script to format your code.

```sh
npm run prettier
```

Run the `check-prettier` script to check code formatting.

```sh
npm run check-prettier
```

#### Code analyses

The vizzu-story project is analysed with `eslint`.

Run the `check-eslint` script to run code analyses.

```sh
npm run check-eslint
```

Run the `eslint` script to solve the fixable problems.

```sh
npm run eslint
```

#### Testing

The vizzu-story project is tested with `jest` testing framework.

Run the `test` script to run the tests.

```sh
npm test
```

### Release

vizzu-story is distributed on [npm](https://www.npmjs.com/package/vizzu-story). **Note:** You need to be an administrator to release the project.

If you want to release vizzu-story follow the steps below.

- You should increase the version number in `package.json`. The version bump should be in a separated commit.

- Generate the release notes and publish the new release on [Releases](https://github.com/vizzuhq/vizzu-ext-js-story/releases).

 **Note:** Publishing a new release will automatically trigger the `release` workflow which builds and uploads the vizzu-story package to [npm](https://www.npmjs.com/package/vizzu-story).

You can build the package before a release with the `build` script.

```sh
npm run build
```
