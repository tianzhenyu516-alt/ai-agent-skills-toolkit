---
name: rt-thread
description: Develop RT-Thread firmware with BSP, threading, synchronization, device drivers, and target validation in mind.
---

# rt-thread

Use this skill for the named platform or workflow. Apply only instructions relevant to the user's actual target; do not assume tools, hardware, or services are installed.

## Confirm the hardware and documents first

Before assigning pins, configuring peripherals, or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** Inspect those documents and the current project before giving a specific pinout. If the user has not supplied or identified authoritative hardware documentation, give only general guidance and clearly mark any candidate mapping as unverified. Do not silently reuse pin assignments from a different board or chip.

If a supplied schematic conflicts with local notes, follow the schematic and explain the discrepancy.

## Inspect the project

Inspect the RT-Thread version, BSP, selected chip, build system, Kconfig/rtconfig, memory configuration, and drivers. Locate optional CubeMX or Studio tools locally rather than relying on another computer's path.

## Make the change

Check thread priorities and stack sizes, scheduler interactions, IPC ownership, interrupt context rules, tick timing, and device lifecycle. Handle allocation failure, queue overflow, timeouts, and watchdog recovery explicitly.

## Verify and report

Build the BSP and review memory output. If the board is connected, test boot logs, threads, interrupts, peripheral I/O, and fault paths; otherwise report build-only verification and provide target steps.

Report what changed, evidence from commands or measurements actually performed, and what remains unverified.
