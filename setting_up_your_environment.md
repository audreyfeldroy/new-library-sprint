# Setting Up Your Environment

Before generating your package, make sure you have the two tools the template relies on: **uv** and **just**.

## Install uv

uv is a fast Python package manager that handles virtual environments, dependencies, and running tools. If you don't have it yet:

On macOS/Linux:

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

On Windows:

```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Verify it's working:

```
uv --version
```

## Install just

just is a command runner. The generated package uses it for common tasks like testing, linting, and releasing.

On macOS:

```
brew install just
```

On Linux:

```
# Via prebuilt binaries
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to ~/bin
```

See [just.systems](https://just.systems/man/en/installation.html) for other installation methods.

Verify:

```
just --version
```

## You don't need to install Cookiecutter

The `uvx` command can run Cookiecutter packages directly without installing anything. When you run `uvx cookiecutter-pypackage` in the next step, uv downloads and runs it in a temporary environment automatically.

## Summary

You have uv and just installed. Next, you'll generate your package skeleton with a single command.
