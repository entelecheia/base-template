# base-template

[![GitHub Super-Linter](https://github.com/entelecheia/base-template/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/marketplace/actions/super-linter)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/f5d47f43f3ba4f1eb5f1d5140d2c69cd)](https://www.codacy.com/gh/entelecheia/base-template/dashboard?utm_source=github.com&utm_medium=referral&utm_content=entelecheia/base-template&utm_campaign=Badge_Grade)

A base template for CI/CD workflows

## Usage

### Create a new repository

1. Click the `Use this template` button
2. Enter a name for your repository
3. Click `Create repository from template`

### Configure the repository

1. Click the `Settings` tab
2. Click `Secrets and variables`
3. Click `Actions`
4. Click `New repository secret`, and add the following secrets:

    - `GH_TOKEN`: A GitHub [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token). The token should have the `repo` scope to allow the workflow to push to the repository.
    - `NPM_TOKEN`: generated from [npmjs.com](https://www.npmjs.com/).

### Configure the workflow

### Push a commit

### Initial release

Push a commit to the `main` branch with the message `feat: initial commit`

## Features

- [x] Linting
- [x] Automated Release Draft
- [x] Semantic versioning
- [x] Secrets management

## Workflows

### CI (Continuous Integration)

#### [Lint Code Base](.github/workflows/ci-linter.yaml)

The `Lint Code Base` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Lint the codebase with GitHub's [Super-Linter](https://github.com/github/super-linter).

#### [Docs to PDF](.github/workflows/ci-build.yaml)

The `Docs to PDF` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Build the documentation to PDF with [Markdown to PDF](https://github.com/BaileyJM02/markdown-to-pdf)

### CD (Continuous Deployment)

The `CD` workflow runs on every push of a tag to the repository.

- [x] Docker image build

## Derived Templates

This template is used to create the following templates:

- [python-template](https://github.com/entelechiea/python-template)
- [pypi-template](https://github.com/entelechiea/pypi-template)
- [jupyter-book-template](https://github.com/entelechiea/jupyter-book-template)

## References

- [Semantic Versioning](https://semver.org/)
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- [semantic-release](https://github.com/semantic-release/semantic-release)
- [Semantic Release Action](https://github.com/cycjimmy/semantic-release-action)
- [Git Semantic Version](https://github.com/marketplace/actions/git-semantic-version)

## License

[MIT](LICENSE)
