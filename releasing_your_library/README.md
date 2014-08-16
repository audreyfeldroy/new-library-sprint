# Releasing Your Library

## Steps

1. Create a GitHub repo.
2. Push your package code to GitHub.

    ```
    cd repo_name
    git init
    git add .
    git commit -m "Initial commit"
    git push -u origin master
    ```

3. Register your package on PyPI.

    ```
    python setup.py sdist register
    ```

4. Do your first release.

TODO get simplified instructions from https://gist.github.com/audreyr/5990987

## Summary

You have now released your library:

* On GitHub as an open-source project
* On PyPI as an open-source Python package

Now others can use your library in their projects. They can even contribute back with bug fixes and new features.
