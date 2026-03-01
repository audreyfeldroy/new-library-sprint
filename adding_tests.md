# Adding Your Code and Tests

## Put your code in the package

1. Find the main module inside `src/`. It will be named after your package (with underscores). For our example, that's `src/text_cleanser/__init__.py` or a module file inside that directory.

2. Paste in your function(s). For example:

    ```python
    # src/text_cleanser/__init__.py

    def clean_whitespace(text: str) -> str:
        """Normalize whitespace in text.

        Collapses multiple spaces, tabs, and newlines into single spaces,
        and strips leading/trailing whitespace.
        """
        return " ".join(text.split())
    ```

3. Verify the import works:

    ```
    uv run python -c "from text_cleanser import clean_whitespace; print(clean_whitespace('  hello   world  '))"
    ```

    You should see: `hello world`

## Write tests

Open the test file in `tests/`. You'll find a starter test. Replace it with real tests for your code:

```python
from text_cleanser import clean_whitespace


def test_collapses_multiple_spaces():
    assert clean_whitespace("hello   world") == "hello world"


def test_strips_leading_trailing():
    assert clean_whitespace("  hello  ") == "hello"


def test_normalizes_tabs_and_newlines():
    assert clean_whitespace("hello\t\tworld\n\nfoo") == "hello world foo"


def test_empty_string():
    assert clean_whitespace("") == ""


def test_already_clean():
    assert clean_whitespace("hello world") == "hello world"
```

### Tips for good tests

- **Test the happy path.** What should happen with normal input?
- **Test edge cases.** Empty strings, very long strings, special characters.
- **Test that wrong input gives the right error.** If your function should raise an exception, test for it.
- **One assertion per test** keeps failures easy to diagnose.
- **Name your tests after what they verify**, not what they call.

## Run everything

The fastest way to check your work is:

```
just qa
```

This runs formatting, linting, type checking, and tests in one command. You should see something like:

```
ruff format .
ruff check .
pyright
uv run pytest
========================= test session starts ==========================
collected 5 items

tests/test_text_cleanser.py .....                                [100%]

========================== 5 passed in 0.01s ===========================
```

All green! If ruff or pyright flag anything, fix those issues before moving on. The error messages are usually clear about what to change.

You can also run just the tests if you want a quicker feedback loop while writing code:

```
just test
```
