---
name: request-code-review
description: Prepare a focused review request with a precise diff, requirements, risk areas, and verification evidence.
---

# Request code review

Use this skill when a user wants a change reviewed or needs a reviewer-ready summary.

1. Determine the intended review range from the branch base, pull request, or user-specified revisions. Include all commits in the task; do not assume `HEAD~1` is sufficient.
2. Read the diff and the acceptance criteria. Summarize the concrete behavior before and after the change.
3. List areas that need careful review: changed interfaces, migrations, security boundaries, failure handling, concurrency, and any hardware or deployment assumptions.
4. Include verification evidence: tests and builds actually run, results, and remaining gaps. Provide reproduction steps when useful.
5. Prepare a concise reviewer brief with links or file paths and focused questions. If a reviewer or review service is available and the user authorized sending, submit it; otherwise give the user the ready-to-send brief.

Do not invent test results or assert approval from a reviewer who has not reviewed the change.
