# Releasing Your Library

This is the home stretch. You'll push to GitHub, set up Trusted Publishing, and get your package on PyPI.

## Push to GitHub

1. Create a new repository on GitHub. You can do this from the command line:

    ```
    gh repo create your-username/text-cleanser --public --source=. --push
    ```

    Or create it on [github.com/new](https://github.com/new) and push manually:

    ```
    git init -b main
    git add .
    git commit -m "Initial commit"
    git remote add origin https://github.com/your-username/text-cleanser.git
    git push -u origin main
    ```

2. Check that GitHub Actions CI is passing. Go to your repo's **Actions** tab. You should see the CI workflow running formatting, linting, type checking, and tests.

## Enable GitHub Pages for docs

1. In your repo, go to **Settings > Pages**.
2. Under **Source**, select **GitHub Actions**.
3. Re-run the Documentation workflow from the Actions tab if needed.

Your docs will be live at `https://your-username.github.io/text-cleanser/`.

## Set up Trusted Publishing on PyPI

Trusted Publishing lets GitHub Actions publish to PyPI automatically when you tag a release. No API tokens to manage.

1. Log in to [pypi.org](https://pypi.org/manage/account/publishing/).
2. Scroll to **"Add a new pending publisher"**.
3. Fill in:
    - **PyPI project name**: `text-cleanser` (your package name)
    - **Owner**: your GitHub username
    - **Repository name**: `text-cleanser` (your repo name)
    - **Workflow name**: `publish.yml`
    - **Environment name**: `release` (or leave blank, depending on your workflow)
4. Click **"Add"**.

That's it. PyPI now trusts your GitHub Actions workflow to publish this package.

## Publish your first release

1. Make sure everything passes:

    ```
    just qa
    ```

2. Create a version tag and push it:

    ```
    just tag
    ```

    This creates a git tag matching the version in `pyproject.toml` and pushes it to GitHub.

3. Go to your repo's **Actions** tab. You should see the publish workflow running. It builds your package, signs it with Sigstore, and uploads it to PyPI.

4. Once it finishes, verify it works:

    ```
    pip install text-cleanser
    ```

    Or better yet, ask a neighbor at the sprint to install it!

## Celebrate

You are now a published Python package author. Your package is on PyPI, installable by anyone in the world. Share the link:

```
https://pypi.org/project/text-cleanser/
```

## What's next?

After the sprint, you can:

- **Add more features** and release them: bump the version with `uv version patch`, commit, and `just tag`
- **Respond to issues and PRs** from users
- **Add badges** to your README (CI status, PyPI version, Python versions)
- **Tell people about it.** Post on social media, write a blog post, present at your local meetup.
