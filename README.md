# base-template
A base template for CI/CD workflows

## Usage

### Create a new repository

1. Click the `Use this template` button
2. Enter a name for your repository
3. Click `Create repository from template`

### Configure the repository

1. Click the `Settings` tab
2. Click `Secrets`
3. Click `New repository secret`

### Configure the workflow

1. Click the `.github/workflows` folder

### Push a commit

1. Click the `Code` tab

## Features

- [x] Linting
- [x] Automated Release Draft
- [x] Semantic versioning
- [x] Secrets management

## Workflows

### CI

The `CI` workflow runs on every push to the repository.

- [x] Linting

### CD

The `CD` workflow runs on every push of a tag to the repository.

- [x] Docker image build

## Secrets

### Docker

- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`

### GitHub

- `GITHUB_TOKEN`

### Semantic Versioning

- `SEMVER_BUMP`

## Derived Templates

This template is used to create the following templates:

- [python-template](https://github.com/entelechiea/python-template)
- [pypi-template](https://github.com/entelechiea/pypi-template)
- [jupyter-book-template](https://github.com/entelechiea/jupyter-book-template)

## References

- [Git Semantic Version](https://github.com/marketplace/actions/git-semantic-version)

## License

[MIT](LICENSE)
