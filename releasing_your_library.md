# Releasing Your Library


## Releasing on GitHub

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
    python setup.py register
    ```

    That should generate the following:

    ```
    running egg_info
    writing upper_casing.egg-info/PKG-INFO
    writing top-level names to upper_casing.egg-info/top_level.txt
    writing dependency_links to upper_casing.egg-info/dependency_links.txt
    reading manifest file 'upper_casing.egg-info/SOURCES.txt'
    reading manifest template 'MANIFEST.in'
    warning: no previously-included files matching '__pycache__' found under directory '*'
    warning: no previously-included files matching '*.py[co]' found under directory '*'
    writing manifest file 'upper_casing.egg-info/SOURCES.txt'
    running check
    Registering upper_casing to http://pypi.python.org/pypi
    Server response (200): OK
    ```

    It's that last line is important. It should say, `Server response (200): OK`. If
    it doesn't please read the Troubleshooting chapter for answers.

## Registering on PyPI

Note: If you've already done this in the past, you can skip to the next section.

TODO this whole section


## Releasing on PyPI

From the command-line

    ```
    python setup.py publish
    running sdist
    running egg_info
    creating upper_casing.egg-info
    writing upper_casing.egg-info/PKG-INFO
    <snip a lot of stuff for brevity>
    Submitting dist/upper_casing-0.1.0.tar.gz to http://pypi.python.org/pypi
    Server response (200): OK
    Submitting /Users/danny/pydanny/cookiecutter-pymodule/upper_casing/dist/upper_casing-0.1.0-py2.py3-none-any.whl to http://pypi.python.org/pypi
    Server response (200): OK
    You probably want to also tag the version now:
      git tag -a 0.1.0 -m 'version 0.1.0'
      git push --tags
    ```

    Again, look for the lines that say, `Server response (200): OK`. These mark a
    successful upload of your new library.



TODO possible simplified instructions from https://gist.github.com/audreyr/5990987

## Summary

You have now released your library:

* On GitHub as an open-source project
* On PyPI as an open-source Python package

Now others can use your library in their projects. They can even contribute back with bug fixes and new features.
