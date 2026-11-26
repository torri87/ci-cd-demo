# CI Minimal Demo

A small Node.js project used to demonstrate automated testing with GitHub Actions.

## Requirements

- Node.js 18.x
- npm

## Run locally

From the repository root, install the locked dependencies and run the test suite:

```sh
npm ci
npm test
```

The Jest tests cover adding two numbers and rejecting non-number arguments.

## Continuous integration

The `CI` workflow in `.github/workflows/ci.yml` runs on every push and pull
request. It checks out the repository, sets up Node.js 18.x with npm dependency
caching, installs dependencies with `npm ci`, and runs the test suite with
`npm test`.

This project does not currently configure a linter or generate coverage/JUnit
reports, so the workflow has no lint step or test artifacts to upload.
