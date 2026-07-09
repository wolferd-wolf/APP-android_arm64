# Automation reports

Every CI run of the build workflows writes a timestamped Markdown file here
(`YYYY-MM-DD_HHMMSS-<stage>.md`), committed as a workflow artifact and, once
we're confident the pipeline is stable, directly back to this folder.

Each report records:
- what was triggered and why
- exact steps that ran
- what was deliberately skipped in that run
- pass/fail status
- a plain-language note on what to check next if it failed

This exists so a failed run is diagnosable from the report alone, without
re-reading the full raw Actions log every time. Nothing here is auto-deleted;
treat it as a running history of what's been tried, including failed
attempts - those are as useful as the successful ones for this project.
