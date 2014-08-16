# Creating a skeleton Python package

Every Python package contains certain files.

## Overview

You will generate the skeleton for a bare-bones Python package with Cookiecutter and cookiecutter-pypackage.

Here's what you'll do:

1. Take 1 or more Python code snippets and turn them into a reusable library
2. Put it on GitHub
3. Register/upload it to the Python Package Index

## Steps

1. Run Cookiecutter with cookiecutter-pymodule:

    ```
    $ cookiecutter https://github.com/pydanny/cookiecutter-pymodule.git
    ```

2. Answer the prompts:

    ```
    $ cookiecutter https://github.com/pydanny/cookiecutter-pymodule
    module_name (default is "The name of the to-be-packaged model.")? upper_casing
    full_name (default is "Roberta Roberts")?
    email (default is "roberts@example.com")?
    github_username (default is "roberta-example")?
    short_description (default is "This package does X")? Upper cases strings
    release_date (default is "2014-01-11")?
    console_script_name (default is "")?
    ```

3. Examine the directory that was generated.

    ```
    ls
    cd repo_name
    ls
    ```

## Summary

You now have a Python package, but other than the boilerplate it's still empty.

Next, you'll put your Python code into your Python package.
