# Troubleshooting

If you run into a problem not listed here, please submit a pull request with:

* Description of the problem
* The exact commands that you ran, and the error message or other problem that you encountered
* Steps to follow to resolve the problem

## Installing Cookiecutter

### Oh no! I have an old version of Cookiecutter

To upgrade, run:

    pip install -U cookiecutter

### ImportError: Fix: pip install wheel

If you try to `python setup.py publish` your project without the Wheel package
installed, you'll get an error like:

    python setup.py publish
    Traceback (most recent call last):
      File "setup.py", line 18, in <module>
        raise ImportError("Fix: pip install wheel")
    ImportError: Fix: pip install wheel

In order to correct this problem, do as the error says from the command-line:

    pip install wheel

## Other problems

Ask for help.
