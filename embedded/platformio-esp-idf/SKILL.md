---
name: platformio-esp-idf
description: Develop PlatformIO projects that use ESP-IDF with environment-specific configuration, component, build, and monitor checks.
---

# platformio-esp-idf

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If the target matches a local draft, compare against [local pin notes](references/local-pin-notes.md) **only after** confirming the board documentation.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Read platformio.ini, selected environment, board, framework version, build flags, partitions, and component dependencies. Do not assume a generic ESP32 pin map applies to the actual board.

## Make the change

Keep configuration in the project's established files and avoid mixing Arduino APIs into a pure ESP-IDF environment. Check peripheral pins, RTOS task and ISR behavior, serial framing, and memory allocation against the chosen framework.

## Verify and report

Build the selected PlatformIO environment. If device access is available, verify upload, serial monitor, boot, and target behavior; otherwise state that only the build was checked.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
