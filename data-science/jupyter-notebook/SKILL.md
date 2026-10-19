---
name: jupyter-notebook
description: Create, edit, and validate self-contained Jupyter notebooks for experiments or tutorials without external templates.
---

# Jupyter notebook

Use this skill to create or revise `.ipynb` files for an experiment, analysis, or tutorial. No bundled assets or helper scripts are required.

## Plan the notebook

- Identify the audience, question, available data, kernel, and dependencies. For private data, use a documented local path or a synthetic sample rather than committing the data.
- Choose an experiment structure (question, setup, method, results, limitations) or tutorial structure (goal, prerequisites, short steps, exercises, recap).

## Build or edit

- Use the notebook format supported by the environment; prefer `nbformat` when installed. Give each section a concise Markdown heading and keep code cells small enough to inspect independently.
- Place imports and configuration near the top. Use reproducible random seeds when randomness affects results. Avoid absolute personal paths, credentials, and network-dependent examples unless essential.
- Make units, expected shapes, and assumptions explicit. Separate source data from derived output. Do not embed private data, huge outputs, or hidden state.
- When editing an existing notebook, preserve useful metadata and intentional outputs. Remove only stale or sensitive outputs.

## Validate

- Parse the final notebook as valid `.ipynb`. Execute it from a clean kernel when dependencies and safe data are available.
- Check cell order, missing variables, broken relative paths, unexpectedly large outputs, and nonportable configuration.
- Report execution status and any dependencies or private inputs needed to reproduce results.
