# Execution

Scripts Claude writes for the mechanical steps of a workflow: pulling data from an API, filling a template, building a report.
Same input, same output, every time.

- One job per script. Reuse before writing a new one.
- Keys come from `.env`, never written into the script.
- Temporary files go in `.tmp/` (not saved to GitHub).
- Every script is called by a directive in `directives/`.
