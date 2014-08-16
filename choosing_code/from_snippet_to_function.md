# From Snippet to Function

If you're starting with a Python script, you may need to turn your code into 1 or more functions.

However, if you're starting with functions, classes, or other reusable units of Python, you can skip this part.

## Encapsulating the code

Your snippet of code should be encapsulated in a function, otherwise packaging
the code won't be so useful. For example, code like this needs to be placed
in a function:

    ```python
    # upper_casing.py
    import sys

    # Get the input value from the user
    value = sys.argv[1]

    # Display the value in upper cased format.
    print(value.upper())
    ```

Here is how we encapsulate the previous code into a function:

    # upper_casing.py
    import sys

    # Define the main function of our program
    def main(value):
        """Uppercases the value"""
        # return the value passed into main as an upper-cased string
        return value.upper()

    if __name__ == "__main__":
        # Get the input value from the user
        value = sys.argv[1]

        # Run the value through the main function
        value = main(value)

        # Display the result via the print function
        print(value)

What's important about this example is that we've isolated the core
functionality of the code snippet into the `main()` function. We've done our
best to ensure that the encapsulated code can be easily reused in other
projects. The same can't really be said about accepting the input value
from the user, or in this case, even the `print()` statement.

Whatever you choose for your own snippet should be isolated in a similar
manner, reducing it to its most atomic level of functionality.

