---
name: embedded-systems
description: Develop and review microcontroller firmware with attention to hardware limits, interrupts, timing, and validation on the target board.
---

# Embedded systems

Use this skill when implementing or reviewing firmware for an MCU, board, peripheral, or RTOS task.

## Establish the target

- Before assigning pins or choosing register values, ask: **“请说明你现在使用的芯片完整型号、开发板/模组型号与硬件版本，并提供数据手册、开发板原理图或引脚表的链接或本地路径。”** If the project already identifies these reliably, confirm them from the project and documents. Without authoritative hardware documentation, give only general guidance and label any suggested mapping unverified.
- Identify the exact MCU/board, SDK or HAL version, compiler, memory budget, clock tree, pin map, peripheral wiring, and build command from the repository. Ask only for details that cannot be determined locally.
- Read the existing startup, linker, clock, interrupt, and peripheral configuration before changing firmware. Do not invent register names or HAL APIs; consult the installed headers or official vendor documentation when uncertain.
- State assumptions when hardware is unavailable. Do not claim on-board behavior was verified by a host-only build.

## Implement

- Keep interrupt handlers bounded: clear the correct source, capture or enqueue work, and defer blocking operations. Check ISR-safe RTOS APIs and interrupt-priority rules for the installed RTOS.
- Protect shared state deliberately with atomics, short critical sections, or a queue. Check DMA buffer ownership, alignment, and cache coherency where applicable.
- Bound all buffers, frame lengths, retries, and timeouts. Define error recovery for disconnected sensors, corrupt frames, and peripheral failures.
- Prefer clear peripheral ownership and explicit initialization order. Avoid dynamic allocation in time-critical paths unless the project already proves it safe.
- Treat power, stack, RAM, Flash, latency, and watchdog behavior as measurable constraints rather than assuming an optimization helps.

## Validate and report

- Run the project's build and any available static or host tests. Check compiler warnings and generated memory-size reports when present.
- For hardware-dependent behavior, provide a short board test: setup, input stimulus, expected serial/logical/electrical output, and failure indication.
- Report what was compiled, what was tested on hardware, and what remains unverified.
