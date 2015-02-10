# Adding Docs

## Steps

1. Look at the skeleton documentation for your new skeleton package. That is, look inside the `docs/` folder at the `.rst` files. Open those files in your favorite text editor or IDE.
2. Modify one of the `.rst` files. For example, you probably need to update `docs/usage.rst` with proper instructions.
3. From your package directory, build the docs from the command line:

    ```
    $ make docs
    ```

You should see a browser open with the rendered HTML version of your docs.

Compare the docs with the `.rst` files. Look for parts that need to be filled in. Edit your `.rst` files and rebuild the docs.
