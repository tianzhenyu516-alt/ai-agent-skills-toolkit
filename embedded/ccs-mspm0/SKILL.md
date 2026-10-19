---
name: ccs-mspm0
description: Work on TI Code Composer Studio and MSPM0 firmware using project-specific SDK, SysConfig, build, and debug evidence.
---

# ccs-mspm0

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Inspect the CCS project, MSPM0 part number, SDK version, SysConfig files, linker command file, clock settings, and debugger before editing. Discover CCS and SDK paths from the local environment or project settings; never assume another person's workspace path.

## Make the change

Keep generated SysConfig code separate from application changes. Check pin multiplexing, interrupt priorities, clock dependencies, timer/PWM units, and peripheral ownership against the installed SDK and board schematic.

## Verify and report

Build the actual project configuration. If a supported probe and target are available, test flash, reset, and relevant signals; otherwise report build-only verification and provide a hardware test procedure.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
