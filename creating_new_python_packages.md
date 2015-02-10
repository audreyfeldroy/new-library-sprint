# Creating a skeleton Python package

Every Python package contains certain files.

## Overview

You will generate the skeleton for a bare-bones Python package with Cookiecutter and cookiecutter-pypackage.

Here's what you'll do:

1. Take 1 or more Python code snippets and turn them into a reusable library
2. Put it on GitHub
3. Register/upload it to the Python Package Index

## Steps

1. Run Cookiecutter with cookiecutter-pypackage:

    ```
    $ cookiecutter https://github.com/audreyr/cookiecutter-pypackage.git
    ```

2. Answer the prompts:

    ```
    $ cookiecutter https://github.com/audreyr/cookiecutter-pypackage
    full_name (default is "Audrey Roy")? Roberta Roberts
    email (default is "audreyr@gmail.com")? roberta@example.com
    github_username (default is "audreyr")? robertaexample
    project_name (default is "Python Boilerplate")? Uppercasing
    repo_name (default is "boilerplate")? uppercasing
    project_short_description (default is "Python Boilerplate contains all the boilerplate you need to create a Python package.")? Uppercasing uppercases strings for you.
    release_date (default is "2014-01-11")? 2015-02-09
    year (default is "2014")? 2015
    version (default is "0.1.0")? 0.1.0
    ```

3. Examine the directory that was generated.

    ```
    ls
    cd uppercasing
    ls
    ```

## Summary

You now have a Python package. But other than the boilerplate, it's still empty.

Next, you'll put your Python code into your Python package.
