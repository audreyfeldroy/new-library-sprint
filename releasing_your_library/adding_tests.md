# Bringing Your Code In

## Steps

1. Look at the `.py` files for your new skeleton package. The one you are looking for is what your package is called. Open that module in your favorite text editor or IDE.
2. Paste in your code.
3. Run the tests from the command-line:

    ```
    py.test
    ====================== session starts ==================
    platform darwin -- Python 2.7.5 -- py-1.4.23 -- pytest-2.6.1
    collected 1 items

    test_upper_casing.py .

    ================ 1 passed in 0.01 seconds ==============
    ```

If you open your test file (test_upper_casing in this example), you will discover
a single, useless test:

```python
import pytest
import upper_casing


def test_the_obvious():
    assert True == True


if __name__ == '__main__':
    pytest.main()
```

Let's change the test so it is actually useful.


```python
import pytest
import upper_casing


def test_upper_case():
    assert upper_casing.upper_casing("halo") == "HALO"

def test_to_fail():
    assert upper_casing.upper_casing("halo") != "halo"


if __name__ == '__main__':
    pytest.main()
```

Run the test again:

    $ py.test
    ====================== session starts ==================
    platform darwin -- Python 2.7.5 -- py-1.4.23 -- pytest-2.6.1
    collected 1 items

    test_upper_casing.py ..

    ================ 2 passed in 0.01 seconds ==============

Hooray! actually useful tests passed!