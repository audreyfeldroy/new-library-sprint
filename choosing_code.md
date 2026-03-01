# Choosing Code

The hardest part of creating a new Python library is coming up with a good idea. But it doesn't have to be a big idea.

## Pick something useful

Look for code you've written (or want to write) that does one thing well:

- A useful function you copy between projects
- A few related utility functions
- A class that wraps something awkward into something clean
- A context manager
- A decorator
- A CLI tool you keep rewriting
- A data validation or transformation helper

### How do you know if it's useful?

- You've copied and pasted it from one project to another
- You've seen someone else solve the same problem in a worse way
- You could imagine wanting it in a future project
- You've explained the trick to a colleague more than once

### Keep it small

For this sprint, keep your scope as small as possible. If this is your first Python package, fewer lines of code is better.

Even a useful 3-line function is worth packaging. The package [cached-property](http://pydanny.com/cached-property.html) started as a tiny snippet that seemed too small to be worth it, and became one of the most downloaded packages on PyPI.

## Ideas if you're stuck

- **String utilities**: slugify, truncate with ellipsis, extract emails from text
- **Date/time helpers**: relative time ("3 days ago"), business day calculations, timezone-aware "now"
- **File utilities**: safe temp files, atomic writes, recursive directory hashing
- **Data cleaning**: normalize whitespace, strip accents, convert between naming conventions (camelCase to snake_case)
- **CLI helpers**: colored output, progress bars, yes/no prompts
- **Config helpers**: merge nested dicts, load from environment variables with type casting
- **API utilities**: retry with backoff, rate limiting decorator
- **Math/stats**: running average, percentile calculation, human-readable file sizes
- **Text processing**: Markdown to plain text, word frequency counter, simple template engine

## Don't panic

Your first Python library doesn't have to change the world. It's even okay if it's a bit silly. The point is to learn the workflow of packaging, testing, and publishing. You can always make something more ambitious next time.

What matters is that you walk out of this sprint with a published package.
