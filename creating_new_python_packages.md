# Creating a Skeleton Python Package

Now for the fun part: generating a complete Python package with one command.

## Overview

You'll use [cookiecutter-pypackage](https://github.com/audreyfeldroy/cookiecutter-pypackage) to generate a package skeleton that includes:

- `pyproject.toml` for project configuration
- GitHub Actions CI (lint, type check, test on Python 3.12/3.13/3.14)
- Automated PyPI publishing via Trusted Publishers (no tokens needed)
- pytest for testing
- ruff for linting and formatting
- pyright for type checking
- Typer CLI entry point
- Documentation with Zensical and mkdocstrings
- A `justfile` with commands for all common tasks

## Steps

1. Run the generator:

    ```
    uvx cookiecutter-pypackage
    ```

    That's it. No need to install Cookiecutter first. `uvx` handles everything.

2. Answer the prompts. Here's an example session:

    ```
    full_name [Audrey M. Roy Greenfeld]: Maria Santos
    email [audreyfeldroy@example.com]: maria@example.com
    github_username [audreyfeldroy]: mariasantos
    pypi_package_name [python-boilerplate]: text-cleanser
    project_name [Python Boilerplate]: Text Cleanser
    project_short_description [...]: Clean and normalize messy text data.
    pypi_username [mariasantos]: mariasantos
    author_website []: https://mariasantos.dev
    first_version [0.1.0]: 0.1.0
    ```

    Tips for answering:
    - **pypi_package_name**: Use hyphens for multi-word names (e.g. `text-cleanser`). This is what people will `pip install`.
    - **project_name**: The human-readable name. Can have spaces and capitals.
    - **project_short_description**: One sentence. This shows up on PyPI.
    - **first_version**: `0.1.0` is a great starting point.

3. Explore the generated directory:

    ```
    cd text-cleanser
    ls
    ```

    You'll see:

    ```
    LICENSE           README.md         docs/
    justfile          pyproject.toml    src/
    tests/            .github/
    ```

    Your code goes in `src/text_cleanser/`. The project uses a `src` layout, which prevents accidentally importing local code during testing.

4. Set up the development environment:

    ```
    uv sync
    ```

    This creates a virtual environment and installs your package in editable mode with all dev dependencies.

5. Verify everything works out of the box:

    ```
    just qa
    ```

    This runs formatting, linting, type checking, and tests in one command. It should pass with the starter code.

6. Try the built-in CLI:

    ```
    uv run text-cleanser --help
    ```

    The template includes a Typer-based CLI entry point you can customize later.

## See all available commands

```
just list
```

This shows you everything the justfile can do: run tests, serve docs, tag releases, and more.

## Summary

You now have a fully functional Python package with CI, linting, type checking, testing, docs, and a CLI, all generated from one command. Next, you'll put your code into it.
