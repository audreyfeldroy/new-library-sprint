# Planning Your New Library

Before generating the package, take a few minutes to plan.

## Pick a name

1. **Choose a name for your package.** This is the name people will use with `pip install your-name`. It should be lowercase, short, and descriptive.
2. **Check PyPI.** Search [pypi.org](https://pypi.org/) to make sure the name isn't already taken.
3. **Use hyphens for multi-word names** in the package name (what people `pip install`), like `my-cool-tool`. The import name will use underscores: `import my_cool_tool`.

## Think about the API

Before you write any code, think about how someone would use your package:

```python
# What will the import look like?
from my_package import my_function

# What arguments will it take?
result = my_function("input", option=True)

# What will it return?
print(result)  # What type? What format?
```

Write out a few example calls. This helps you design a clean interface before you get caught up in implementation details.

## Checklist before you proceed

- [ ] You have a name that isn't taken on PyPI
- [ ] You can describe what the package does in one sentence
- [ ] You have at least one function or class ready to package
- [ ] You know what arguments it takes and what it returns
