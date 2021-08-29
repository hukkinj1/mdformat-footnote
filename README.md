# mdformat-footnote

[![Build Status][ci-badge]][ci-link]
[![codecov.io][cov-badge]][cov-link]
[![PyPI version][pypi-badge]][pypi-link]

Footnote format addition for [mdformat](https://github.com/executablebooks/mdformat).

## Development

This package utilises [flit](https://flit.readthedocs.io) as the build engine, and [tox](https://tox.readthedocs.io) for test automation.

To install these development dependencies:

```bash
pip install tox
```

To run the tests:

```bash
tox
```

and with test coverage:

```bash
tox -e py39-cov
```

The easiest way to write tests, is to edit tests/fixtures.md

To run the code formatting and style checks:

```bash
tox -e py39-pre-commit
```

or directly

```bash
pip install pre-commit
pre-commit run --all
```

To run the pre-commit hook test:

```bash
tox -e py39-hook
```

## Publish to PyPi

Either use flit directly:

```bash
pip install flit
flit publish
```

or trigger the GitHub Action job, by creating a release with a tag equal to the version, e.g. `v0.0.1`.

Note, this requires generating an API key on PyPi and adding it to the repository `Settings/Secrets`, under the name `PYPI_KEY`.

[ci-badge]: https://github.com/gaige/mdformat-footnote/workflows/CI/badge.svg?branch=master
[ci-link]: https://github.com/gaige/mdformat-footnote/actions?query=workflow%3ACI+branch%3Amaster+event%3Apush
[cov-badge]: https://codecov.io/gh/gaige/mdformat-footnote/branch/master/graph/badge.svg
[cov-link]: https://codecov.io/gh/gaige/mdformat-footnote
[pypi-badge]: https://img.shields.io/pypi/v/mdformat-footnote.svg
[pypi-link]: https://pypi.org/project/mdformat-footnote
