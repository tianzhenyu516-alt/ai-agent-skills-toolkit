---
name: autopilot-workflow
description: Carry a scoped software task from requirements through implementation and validation with explicit checkpoints and honest status reporting.
---

# Autopilot workflow

Use this skill when the user asks an agent to take a software task from an idea or issue to a verified result. Respect the user's requested scope and stop points.

1. Inspect the repository, instructions, existing behavior, and available tests. Identify the concrete outcome and any missing information that materially changes implementation.
2. Break the work into a small sequence of outcomes. State assumptions only where needed; continue with reversible work while waiting for answers.
3. Implement in the repository's conventions. Preserve unrelated changes and use focused edits. Recheck the user-visible behavior after each meaningful step.
4. Run the relevant build, tests, lint, or manual checks. When something fails, investigate the actual cause and repair it; do not loop indefinitely or hide repeated failure.
5. Review the final diff for correctness, data exposure, and scope. Report what changed, the checks run, and any remaining limitations.

External publication, deployment, account changes, or messaging still require the authorization applicable to those actions. This skill does not assume access to a particular plugin, agent API, command palette, or background service.
