# ai-skill-platformio-esp-idf

PlatformIO and ESP-IDF integration skill.

## Purpose

Develop PlatformIO projects that use ESP-IDF with environment-specific configuration, component, build, and monitor checks.

## Install

Copy the `platformio-esp-idf` folder into your AI assistant's skills directory. Then ask the assistant to use the `platformio-esp-idf` skill for a matching project. Start with [`platformio-esp-idf/SKILL.md`](SKILL.md) and keep any referenced board notes with it. No API key, bundled script, or particular plugin is required.

## What to provide

Give the assistant your **exact chip model, development board/module and hardware revision**, plus a **datasheet, board schematic, or pinout document** as a link or local path. Also provide your repository location, goal, and available build or hardware tools. The skill instructs the assistant to ask for these details before suggesting pin assignments.

## Provenance and license

This standalone skill was rewritten from the author's local draft. Machine-specific paths and assumed plugin availability were removed. Hardware and tool names are used descriptively and belong to their respective owners. Newly written text in this repository is available under the [MIT License](LICENSE).

## Related

For general MCU engineering, see [ai-skill-embedded-systems](../embedded-systems).

## Search terms

ai-skills · platformio · esp-idf · esp32 · embedded-systems

