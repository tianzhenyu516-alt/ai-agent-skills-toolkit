---
name: review-feedback
description: Evaluate code review feedback against the implementation, make justified changes, and verify each fix.
---

# Review feedback

Use this skill when review comments or requested changes need to be assessed and implemented.

1. Read the complete feedback and locate each referenced code path. Group related comments so a fix does not conflict with another request.
2. Verify the reported behavior in the current revision. If the requirement is ambiguous or the code has changed, identify the exact uncertainty before editing.
3. Decide per comment: fix, ask for clarification, or explain with technical evidence why the suggestion does not apply. Do not agree reflexively.
4. Make the smallest coherent correction. Add or adjust a test when it can demonstrate the reported failure and guard against recurrence.
5. Run the relevant checks. For each comment, report the change and evidence, or give a concise reason it remains unresolved.

Do not claim that a check passed if it was not run. Never send replies to a review service unless the user has authorized that external action.
