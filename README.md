# exemaitch
[![Create and publish a Docker image](https://github.com/xmlabs-io/exemaitch/actions/workflows/build-vscode-linux.yml/badge.svg)](https://github.com/xmlabs-io/exemaitch/actions/workflows/build-vscode-linux.yml)

## Code Quailty
### Pre-commit

This project uses [pre-commit](https://pre-commit.com/) to automatically run `mypy`, `black` and `flake8` before commits.

To setup `pre-commit`, run the following once:

```shell script
$ pre-commit install
```

You can always skip pre-commit git hooks via the `--no-verify` option. But remember: the CI is always watching!

### Running the Checks

To run `mypy`:

```shell script
$ mypy .
```

`mypy` is configured in `mypy.ini`.

To run `flake8`:

```shell script
$ flake8
```

`flake8` is configured in `.flake8`.

To run `black`, checking for issues:

```shell script
$ black --check .
```

To run `black`, fixing issues:

```shell script
$ black .
```


