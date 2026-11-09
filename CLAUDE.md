# Instructions for Claude Code

This repo is one experiment in the playground-gg organisation. Read `README.md` (the question and setup) before writing code. If the README still has `<placeholders>`, help the user fill them in first.

## Hard constraints
- Runs on the user's MacBook (Apple Silicon, 24 GB). Use `torch` with `mps` where relevant, falling back to `cpu`. Do not set up cloud GPUs unless the README explicitly says so.
- Ask the user before: downloading more than ~20 GB, changing macOS system settings, installing system-level packages, or starting a run expected to take more than ~2 hours.
- Never commit model weights, checkpoints, large datasets (> ~5 MB) or large logs. Keep them in `~/playground-cache/` or `.gitignore`d folders.

## How to work
- Start with the cheapest end-to-end run (1 example, few steps), then scale.
- Pin every external revision (model revision hash, git commit, package versions) in `configs/`.
- Fix seeds; record that MPS is not fully deterministic.
- Make long runs resumable and write results incrementally.
- Add small unit tests for anything that computes a metric or a loss. Run `pytest` before committing.
- Save compact results (CSV, small PNG/GIF) in `results/`. Plots: matplotlib, readable labels.
- Keep `README.md` (reference) and `WRITEUP.md` (story) up to date when results change.

## Honesty rules
- No novelty claims. If a result disagrees with a paper, report it with likely reasons; do not tune until it matches.
- Report intervals (bootstrap or across seeds) when comparing settings.
- Keep failed runs and negative results in the write-up.

## Commits
Small, descriptive commits. Do not push without the user's OK.
