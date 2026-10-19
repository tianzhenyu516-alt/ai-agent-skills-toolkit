---
name: python-data-science
description: Create reproducible Python data analysis with explicit inputs, validation, leakage checks, and honest results.
---

# python-data-science

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Identify the question, data provenance, schema, units, target variable, environment, and expected output. Keep private datasets and credentials local; use synthetic fixtures in a public example.

## Make the change

Validate missing values, duplicates, types, and outliers before modeling. Split data before learning preprocessing parameters. Prevent train/test leakage and report metrics appropriate to the task with a baseline and uncertainty where feasible.

## Verify and report

Run scripts or notebooks from a clean environment when possible. Record package versions or lockfiles, random seeds, input assumptions, plots/tables, and limitations. Never invent measured performance.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
