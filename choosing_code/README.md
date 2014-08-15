# Choosing Code!

First of all, **don't panic**. For your first released package you don't need
to release a Python package that changes the world. For your first released
effort it's even okay if your package is a bit silly.

## Suggestions for your first Python package

### Pick something useful

Try to pick something useful that you've written or want to write:

* A useful function
* A few functions that are related somehow
* A class that does something useful
* A useful context manager
* Any other useful snippet

#### How do you know if it's useful?

Here are some signs that a piece of code is useful:

* You've copied and pasted it from one project to another
* You could imagine use cases for wanting it in future projects

### Don't be overambitious

For this sprint, keep your scope as small as possible. If this is your first Python package, the less lines of code, the better.

Even a useful 3-line function is worth packaging.

See [cached-property: Don't copy-paste code](http://pydanny.com/cached-property.html) for a story about a time that Daniel Greenfeld turned a tiny snippet that seemed unworthy of packaging into a useful package.

### Still stuck?

If you have no idea what to work on still, consider:

* Simple string utilities
* Web-Scraping scripts
* Big Data scripts
* Command-line games
* TODO: Add more

## Encapsulating the code

Your snippet of code should be encapsulated in a function, otherwise packaging
the code won't be so useful. For example, code like this needs to be placed
in a function:

    # upper_casing.py
    import sys

    # Get the input value from the user
    value = sys.argv[1]

    # Display the value in upper cased format.
    print(value.upper())

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
manner, reducing it to it's most atomic level of functionality.

[It's time to turn your encapsulated code into a Python package!](/creating_new_python_packages/README.rst)


