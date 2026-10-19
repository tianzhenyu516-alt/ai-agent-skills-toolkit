---
name: hi3861-openharmony
description: Develop Hi3861 OpenHarmony firmware with attention to the actual SDK, board, build system, and peripheral mapping.
---

# hi3861-openharmony

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If the target matches a local draft, compare against [local pin notes](references/local-pin-notes.md) **only after** confirming the board documentation.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Inspect the target board, OpenHarmony distribution and SDK revision, build scripts, board configuration, and schematic. Confirm APIs and build commands from the checked-out source; do not mix incompatible LiteOS or vendor examples.

## Make the change

Keep startup, Wi-Fi, GPIO, UART, timers, and task ownership clear. Validate voltage and pin mappings from the actual board rather than using a hardcoded reference table for all boards. Bound buffers and handle disconnects and timeouts.

## Verify and report

Run the project build. If hardware is available, test boot logs, peripheral signals, and network recovery. Distinguish compilation from real-device validation.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
