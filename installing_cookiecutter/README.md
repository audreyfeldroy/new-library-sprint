# Installing Cookiecutter

Before we do anything else, let's get our environment ready. We'll also need
the [cookiecutter](https://github.com/audreyr/cookiecutter) library to handle
most of the boilerplate code. As mentioned previously, you should already have
`pip` and `virtualenv` (or `virtualenv_wrapper`) available.

> **Info** TODO: Link to instructions on installing these tools

Our first step is to create an stand-alone environment where we can do all of
our work. The tool of choice here is `virtualenv`. From the command-line,
type:

    $ python -m venv cc

> **Info** TODO: Describe doing this with Python 3

What we've done is create a Python virtual environment where we can install
and manage our dependencies. Now it's time to install [cookiecutter](https://github.com/audreyr/cookiecutter).

From the command-line, we type:

    (cc) $ pip install cookiecutter

> **Info** [cookiecutter](https://github.com/audreyr/cookiecutter) is a
command-line utility that creates projects from templates called
'cookiecutters'. Created and led by Audrey Roy, it's a cross-platform tool
designed to expedite project creation. While in this sprint we're using it
for Python, people have created hundreds of JavaScript, Ruby, Lisp, C, C++,
Objective-C templates powered by this tool.

Cookiecutter should take about a minute to install. Once cookiecutter finishes
installing, let's check that it's working okay with a version check:

    (cc) $ cookiecutter --version
    Cookiecutter 0.7.2

If the result is `Cookiecutter 0.7.2`, that means it's time to [find some
code to turn into a Python package](/choosing_code/README.md)!