---
name: keil-uv5-stm32
description: Work on Keil uVision 5 STM32 firmware projects with target-aware build, linker, startup, and debug checks.
---

# keil-uv5-stm32

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Inspect the .uvprojx project, selected target, device family, packs, compiler, startup file, scatter file, and STM32 HAL/LL version. Locate local tools from the environment instead of hardcoded user paths.

## Make the change

Keep Cube-generated code inside designated user sections if regeneration is expected. Check RCC configuration, pin alternate functions, NVIC priorities, DMA ownership, and the actual MCU's memory map before editing peripheral code.

## Verify and report

Build the selected target and inspect warnings and size output. Test flashing and peripheral behavior only with the matching board and probe; otherwise provide a concrete board test checklist.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
