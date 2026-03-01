# New Library Sprint

Create and publish your own Python package in one sprint session.

## PythonAsia 2026

Welcome, sprinters! By the end of today, you'll have a real Python package on PyPI that anyone in the world can `pip install`. Several past sprint participants have gone on to maintain popular packages that started exactly this way.

## Why package your code?

You've probably written a useful function, class, or script that you copy between projects. Packaging it means:

- **Others can use it.** A single `pip install your-package` and they're off.
- **You get tests and CI for free.** The template sets up pytest, GitHub Actions, and linting from the start.
- **You practice real open-source workflow.** Git, GitHub, PyPI, versioning, documentation.

There are over 600,000 packages on PyPI. Yours could be next.

## Who should participate

If you're comfortable writing simple Python scripts or programs, you'll be fine. Knowledge of Python past the "Hello World" basics is recommended.

No packaging experience required. That's what this sprint is for.

## Prerequisites

You'll need:

- **Python 3.12 or higher** installed
- **uv** installed ([installation guide](https://docs.astral.sh/uv/getting-started/installation/))
- **just** installed ([installation guide](https://just.systems/man/en/installation.html))
- **git** installed and configured
- A **GitHub** account
- A **PyPI** account ([register here](https://pypi.org/account/register/))
- A text editor or IDE you're comfortable with
- A snippet, function, or class you'd like to package (or an idea for one)

> **New to uv?** It's the modern way to manage Python projects and tools. It replaces pip, virtualenv, and setuptools in one fast tool.
>
> **New to just?** It's a command runner (like make, but simpler). The template uses it to run tests, linting, docs, and releases with short commands like `just qa`.

## What you'll do

1. **Choose code** to package (or come up with an idea)
2. **Turn it into a function** if it isn't one already
3. **Plan your library** (pick a name, think about the API)
4. **Generate the package skeleton** with `uvx cookiecutter-pypackage` (one command, no install needed)
5. **Drop your code in** and write a couple of tests
6. **Add basic docs**
7. **Push to GitHub** and publish to PyPI
8. **Install your own package** with pip and celebrate

The template gives you a modern Python package with pyproject.toml, GitHub Actions CI, pytest, ruff linting, and automated PyPI publishing out of the box.

Ready? Let's get started.
