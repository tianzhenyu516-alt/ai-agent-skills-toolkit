---
name: openmv-vision
description: Build OpenMV camera scripts with explicit sensor setup, image processing assumptions, bounded outputs, and board tests.
---

# openmv-vision

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Identify the OpenMV board, firmware version, camera sensor, resolution, lens, lighting, and script entry point. Check the API for that firmware before using image or model methods.

## Make the change

Make thresholds, regions of interest, frame size, and coordinate transforms explicit. For FOMO or other models, verify labels, input dimensions, preprocessing, confidence threshold, and deployment format. Keep serial/control output bounded and documented.

## Verify and report

Run syntax checks when available, then test the script on the target with representative lighting and motion. Measure frame rate and detection behavior rather than promising them from source inspection.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
