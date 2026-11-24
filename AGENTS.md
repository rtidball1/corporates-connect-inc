# Rules for my agent

I am a graduate business student building my final project: a product on my own database that a person outside my course can open and use. Treat me as a careful beginner who has never worked as a developer.

## Before you write code

- Read `## The Plan` in `README.md` first, and build what it says. If what I ask for goes beyond the plan, tell me before you write anything, so I can change the plan or cut the idea down.
- When my request is ambiguous, ask me one question before you write anything.

## How to help me

- Write the simplest code that works. Prefer plain `for` loops, `if`, lists and dicts. Use a comprehension, a lambda or a class only when I ask for one.
- Explain, without being asked, any line I could not have written myself, in one sentence. Explain my join and my AI step in full, because I will explain both in my own words in a video.
- If your code skips rows, converts values or changes a type, tell me how many rows it affected.
- Keep answers short. Leave out the preamble, the emoji headings and the summary of what you just did.

## My data and my database

- `db/build.py` builds my database, `db/database.duckdb`, from the files in `db/data/`. To change the data, change those files or the code that writes them. Never edit the database file by hand, and never commit it.
- Never invent data. If a download fails or a source does not have what I need, tell me. Do not fill a table with rows you made up.
- When you add real data, write its source address and the date I downloaded it into `README.md`.
- Before and after every join you write, count the rows, and tell me both numbers.

## Queries

- A value that the person using my product chooses or types goes into the query as a parameter, with `?`. Never put it into the SQL text with an f-string.
- Let the query do the counting and summing, and show the person a summary or the first rows. My product runs on a free Render instance with 512 MB of memory, and loading a whole large table into the page runs it out of memory.

## Keys

- Read every API key from an environment variable. On my computer it comes from `.env`, which is never committed. On Render it comes from the service's settings.
- Never print a key, and never write one into a notebook, a cell's output or any file I commit.

## Notebooks

- My notebooks are marimo files. A name can be defined in only one cell. A cell shows its last expression, so end a chart cell with the chart and never call `plt.show()`.
- I start marimo from the root folder of this repository with `uv run marimo edit`. The product runs with `uv run marimo run <notebook>.py`.

## Environment

- This repository is a uv project, and uv manages everything in it: `uv add` and `uv remove` for packages, `uv run` to run anything, `uv sync` to rebuild the environment on another computer. Never use `pip`, `conda`, `python -m venv` or `uv pip install`, because none of them records the change in `pyproject.toml`.
- Every copy of this repository has a `pyproject.toml` in its root folder. If you cannot find it, I have opened the wrong folder: stop and tell me. Do not create one, and do not install anywhere else.
- My repository is public. Never put an API key, a password or personal data into a committed file.

## Checking work

- Before you tell me something works, run it and show me what it printed. A marimo notebook runs top to bottom with `uv run python <notebook>.py`.
