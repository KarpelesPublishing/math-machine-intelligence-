# The Mathematics of Machine Intelligence: companion notebooks and skills

Companion material for *The Mathematics of Machine Intelligence* (subtitle: *The Shared Mathematics of Brains, Machines, and Human-AI Partnership*) by Jason Karpeles. Each of the 34 chapters has an illustrated interactive reader, a Jupyter notebook that reproduces its calculations and figures, and a skill that an AI assistant can use to teach the chapter.

About the book: https://karpeles.com/publishing/math-machine-intelligence

## What is here

- `notebooks/`: one notebook per chapter, already run, so the results show on GitHub. 34 chapters, 215 demonstrations.
- `skills/`: a master skill for the book ([`skills/mmi-guide`](skills/mmi-guide/SKILL.md)) and one skill per chapter (`mmi-ch01-...` to `mmi-ch34-...`).
- `web/`: the interactive readers as static HTML. Open [`web/companions/math-machine-intelligence/index.html`](web/companions/math-machine-intelligence/index.html) in a browser to use them offline, or copy `web/companions/` to any static web host. [`web/README.md`](web/README.md) explains the layout.

## How to read the demonstrations

The book treats its mathematics as a model of a brain or a machine, not as the thing itself. Each demonstration says where its numbers come from. Where a number comes from the book or a paper the book cites, the demonstration says so. Where the companion built a small example to show the arithmetic, the demonstration labels it as constructed. A simulation here is never a measurement.

## Run the notebooks

You need Python 3.10 or later.

    pip install -r requirements.txt
    jupyter lab

Open any notebook in `notebooks/` and choose Run All.

## Use the skills

Each folder in `skills/` is a self-contained skill. Copy a folder into `~/.claude/skills/` (or your agent's skills folder), for example:

    cp -r skills/mmi-guide ~/.claude/skills/mmi-guide
    cp -r skills/mmi-ch01-making-mind ~/.claude/skills/mmi-ch01-making-mind

Start with the master skill: it routes a question to the right chapter.

## Copyright

Copyright Jason Karpeles. All rights reserved.
