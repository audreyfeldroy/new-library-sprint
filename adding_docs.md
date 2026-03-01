# Adding Docs

Your package template came with a documentation setup. Let's fill it in.

## Update the README

The generated `README.md` already has your project name and description. Update it with:

- A quick usage example showing how to import and call your function
- Installation instructions (`pip install your-package-name`)

A good README example section looks like:

```markdown
## Usage

```python
from text_cleanser import clean_whitespace

clean = clean_whitespace("  hello   world  ")
print(clean)  # "hello world"
```
```

That's often enough for a first release. People can figure out a lot from one clear example.

## Build the docs locally

The template uses mkdocs for documentation. To preview:

```
just docs-serve
```

This starts a local server where you can see your rendered docs. Look through the pages and fill in any sections that need your input, especially the usage page.

## What to document first

For a sprint, focus on:

1. **README.md**: Installation + one usage example. This is what people see first on PyPI and GitHub.
2. **Docstrings**: You already wrote these when you added your code. mkdocstrings will pull them into the docs automatically.

That's enough for a first release. You can always add tutorials, API reference pages, and guides later.
