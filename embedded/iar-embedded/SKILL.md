---
name: iar-embedded
description: Maintain IAR Embedded Workbench projects with toolchain, linker, memory, and target-debug awareness.
---

# iar-embedded

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Inspect the .eww/.ewp project, selected configuration, device, compiler version, include paths, and linker file. Discover the local IAR installation; do not embed one machine's executable path.

## Make the change

Preserve project-defined language options and runtime libraries. Check startup symbols, memory regions, section placement, stack and heap limits, and interrupt vector names against the selected device support package.

## Verify and report

Build the chosen configuration and inspect errors, warnings, and memory output. Use target debugging only when the probe and board are available; describe hardware checks separately.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
