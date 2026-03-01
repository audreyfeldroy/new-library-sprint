# From Snippet to Function

If you're starting with a Python script, you'll need to turn your code into one or more functions. If you already have functions, classes, or other reusable units, skip ahead to [Planning Your New Library](new_library.md).

## Encapsulating the code

Your snippet needs to be encapsulated in a function, otherwise packaging it won't be very useful. For example, code like this needs to be wrapped:

```python
# upper_casing.py
import sys

value = sys.argv[1]
print(value.upper())
```

Here's how to encapsulate it:

```python
# upper_casing.py
import sys


def uppercase(value: str) -> str:
    """Return the value uppercased."""
    return value.upper()


if __name__ == "__main__":
    value = sys.argv[1]
    print(uppercase(value))
```

The key move is isolating the core functionality into `uppercase()`. The function takes an input, returns an output, and doesn't care where the input came from or what happens with the output. That's what makes it reusable.

The `if __name__ == "__main__"` block handles the command-line interface separately, so the function can be imported and used by other code without triggering the CLI behavior.

## Tips for good function design

- **Take inputs as arguments, return outputs as return values.** Avoid reading from stdin or printing inside your function.
- **Add type hints.** They help users understand your API and catch bugs early.
- **Write a one-line docstring.** Describe what the function does, not how.
- **Keep it focused.** If your function does two things, make it two functions.
