---
name: esp32-s3-esp-idf
description: Develop ESP32-S3 firmware with ESP-IDF, FreeRTOS, peripheral, memory, and board-configuration checks.
---

# esp32-s3-esp-idf

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Identify the ESP-IDF version, target, board, sdkconfig, partitions, PSRAM setup, and pin assignments. Use the project's installed component APIs and official docs for the matching version.

## Make the change

Review task ownership, queue and mutex use, stack sizes, ISR-safe APIs, and watchdog behavior. Check DMA and cache constraints before sharing buffers. Avoid assuming PSRAM, USB, Wi-Fi, or a peripheral is enabled on every board.

## Verify and report

Run the project's ESP-IDF build and focused tests. Flash and monitor only when the intended board and port are known. Report firmware size, build result, and any unverified on-board behavior.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
