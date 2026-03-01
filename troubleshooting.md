# Troubleshooting

If you run into a problem not listed here, ask a sprint mentor for help, or submit a pull request with the problem and solution.

## Installing uv

### I don't have uv installed

Follow the official instructions at [docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/).

On macOS/Linux:

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

On Windows:

```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### uv command not found after installation

Restart your terminal, or add `~/.local/bin` to your PATH.

## Installing just

### I don't have just installed

On macOS:

```
brew install just
```

See [just.systems](https://just.systems/man/en/installation.html) for other platforms.

## Generating the package

### uvx cookiecutter-pypackage fails

Make sure uv is installed and up to date:

```
uv self update
```

Then try again:

```
uvx cookiecutter-pypackage
```

## Running tests

### just qa fails with "command not found"

Make sure you've run `uv sync` inside your project directory first. This installs all dev dependencies.

### Import errors when running tests

Make sure you're running from your project's root directory (the one with `pyproject.toml`) and that you've run `uv sync`.

## Publishing to PyPI

### Trusted Publishing not working

Double-check that:
- The **PyPI project name** matches your package name exactly
- The **repository name** matches your GitHub repo name exactly
- The **workflow name** is correct (check `.github/workflows/` for the actual filename)
- You've pushed the tag to GitHub (not just created it locally)

### Package name already taken on PyPI

Pick a different name. You'll need to re-generate the package with `uvx cookiecutter-pypackage` using the new name, then move your code over.

### Build errors

Make sure your `pyproject.toml` is valid:

```
uv run python -c "import tomllib; tomllib.load(open('pyproject.toml', 'rb'))"
```

## Git issues

### I forgot to create a .gitignore

The template includes one. If you accidentally deleted it, create a new one at [gitignore.io](https://www.toptal.com/developers/gitignore/api/python).

### I committed something I shouldn't have

If you haven't pushed yet:

```
git reset HEAD~1
```

This undoes the last commit but keeps your files. Fix the issue, then commit again.

## Other problems

Ask a sprint mentor, or check the [cookiecutter-pypackage issues](https://github.com/audreyfeldroy/cookiecutter-pypackage/issues) for known problems and solutions.
