# base-template

[![GitHub Super-Linter](https://github.com/entelecheia/base-template/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/marketplace/actions/super-linter)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/f5d47f43f3ba4f1eb5f1d5140d2c69cd)](https://www.codacy.com/gh/entelecheia/base-template/dashboard?utm_source=github.com&utm_medium=referral&utm_content=entelecheia/base-template&utm_campaign=Badge_Grade)

A base template for CI/CD workflows with MkDocs and Semantic Release

## Usage

### Create a new repository

1. Click the `Use this template` button
2. Enter a name for your repository
3. Click `Create repository from template`

### Initial release

Push a commit to the `main` branch with the message `feat: initial commit`

### GitHub Pages

1. Modify the contents of the `mkdocs.yaml` file
2. Add content to the `docs` folder
3. Push a commit to the `main` branch
4. Wait for the `Publish docs via GitHub Pages` workflow to complete
5. Go to the `Settings` tab of your repository
6. Scroll down to the `pages` section
7. Select `Deploy from a branch` as the source
8. Select `gh-pages` as the branch and `/(root)` as the folder, then click `Save`

## Features

- [x] Linting
- [x] Automated Release Draft
- [x] Semantic versioning
- [x] Documentation to PDF
- [x] Github Pages deployment (MkDocs)

## Workflows

### CI (Continuous Integration)

#### [Lint Code Base](.github/workflows/ci-linter.yaml)

The `Lint Code Base` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Lint the codebase with GitHub's [Super-Linter](https://github.com/github/super-linter).

### CD (Continuous Deployment)

#### [Docs to PDF](.github/workflows/cd-build.yaml)

The `Docs to PDF` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Build the documentation to PDF with [Markdown to PDF](https://github.com/BaileyJM02/markdown-to-pdf)

#### [Release](.github/workflows/cd-release.yaml)

The `Release` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Create a release draft with [semantic-release](https://github.com/semantic-release/semantic-release)

#### [Publish docs via GitHub Pages](.github/workflows/cd-mkdocs.yaml)

The `Publish docs via GitHub Pages` workflow is automatically triggered whenever there is push activity in `main` or pull request activity towards `main`. It has one job:

- Publish the documentation to GitHub Pages with [MkDocs](https://www.mkdocs.org/)

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
