---
name: arduino-firmware
description: Develop Arduino firmware across supported boards with correct pin mapping, libraries, timing, and hardware checks.
---

# arduino-firmware

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Identify the exact board, core package, clock, voltage, pin map, and installed libraries. Use the project's existing sketch or PlatformIO layout. Check whether APIs differ between AVR, SAMD, ESP32, and other cores before reusing examples.

## Make the change

Keep loop timing explicit; avoid long blocking delays when inputs or communication need service. Bound serial input and buffers. For register-level changes, verify the exact MCU datasheet and avoid presenting one family's addresses as universal.

## Verify and report

Compile for the selected board and inspect warnings. Give a board test with wiring, stimulus, expected serial/output behavior, and what remains untested without hardware.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
