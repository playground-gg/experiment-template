# <experiment-name>

> **Question:** <one sentence: what do I want to find out?>

**Status:** planning · running · done
**Hardware:** MacBook (Apple Silicon, 24 GB) — <change if different>
**Started:** <YYYY-MM-DD>

## Why
<2–3 sentences: what triggered this (a new model, a paper, a tool) and why it is interesting.>

## Setup
- Model / tool: <name + exact revision or version>
- Data: <dataset + split + number of examples>
- What I change: <the one variable being tested>
- What I measure: <metrics>

## Run it
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python scripts/inspect_environment.py
<exact command(s) to reproduce the main result>
```

## Results
<1–3 figures or a small table from `results/`, each with one line of interpretation.>

## What I learned
- <bullet>
- <bullet>

## Limitations
<subset size, hardware, settings that differ from the original paper, etc.>

## References
- <paper / repo / model card>

---
Part of [playground-gg](https://github.com/playground-gg). Write-up: [`WRITEUP.md`](WRITEUP.md).
