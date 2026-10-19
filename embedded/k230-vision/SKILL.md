---
name: k230-vision
description: Develop K230 camera and vision applications with validated image pipeline, model conversion, deployment, and device evidence.
---

# k230-vision

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Identify the K230 board, firmware/SDK version, camera sensor, image format, runtime, and model artifacts. Inspect existing preprocessing and postprocessing before changing inference code. Confirm APIs against the installed SDK.

## Make the change

Keep model input shape, color order, normalization, coordinate transforms, and display/output dimensions consistent. Define bounds for detections and serial messages; separate camera capture, inference, control output, and error recovery.

## Verify and report

Validate syntax or build where supported and compare a small known input through preprocessing and postprocessing. If the board is available, check camera frames, latency, memory, and actual output. Do not claim accuracy or FPS without measurement.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
