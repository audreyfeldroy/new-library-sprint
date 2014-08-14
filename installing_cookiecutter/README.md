# Installing Cookiecutter

Before we do anything else, let's get our environment ready. We'll also need
the [cookiecutter](https://github.com/audreyr/cookiecutter) library to handle
most of the boilerplate code. As mentioned previously, you should already have
`pip` available.

## Overview

[Cookiecutter](https://github.com/audreyr/cookiecutter) is a command-line utility that creates projects from templates called 'cookiecutters'. Created and led by Audrey Roy, it's a cross-platform tool designed to expedite project creation.

While in this sprint we're using it for Python, people have created Cookiecutter project templates that set up packaging boilerplate for JavaScript, Ruby, Lisp, C, C++, Objective-C, and other languages.

## Steps

Now it's time to install [cookiecutter](https://github.com/audreyr/cookiecutter).

From the command line, we type:

    $ pip install cookiecutter

> **Info** You may need to use `sudo` before this.

Cookiecutter should take about a minute to install. Once cookiecutter finishes
installing, let's check that it's working okay with a version check:

    $ cookiecutter --version
    Cookiecutter 0.7.2

If the result is `Cookiecutter 0.7.2`, that means it's time to [find some
code to turn into a Python package](/choosing_code/README.md)!

## FAQ

### Should I install cookiecutter into a virtualenv?

You can if you want, but you don't have to.

Typically many people install it systemwide, as with other useful command-line utilities.

### What if I don't have pip?

You can also install it via `easy_install`, or via your system's package manager. There are packages for Homebrew, Ubuntu, and Debian. (TODO: add link to details)

## Summary

You now have Cookiecutter installed and ready to go on your computer.

In **Creating New Python Packages**, you will be using Cookiecutter to grab a project template containing boilerplate for starting an open-source Python package.
