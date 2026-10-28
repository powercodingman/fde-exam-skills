# Evidence gate

Match each claim to fresh, inspectable evidence.

| Claim | Evidence |
|---|---|
| Core workflow works | Run the workflow with a representative fixture and record the observed result |
| Business rule is correct | Behavior test at the public seam with an independently derived expected value |
| Failure is handled | A failing or exceptional input and the visible recovery path |
| Data persists | Reload or restart check plus the stored-state boundary |
| Test suite passes | Fresh full test command, exit code, and failure count |
| Build is usable | Fresh production build command and exit code |
| Requirement is met | Acceptance item linked to the implementing file and verification result |
| Tool helped | Baseline problem, tool output, measurable change, risk, and fallback in `TOOLING.md` |

Before submission:

1. Run the full test and build commands.
2. Exercise the highest-value path and one failure path.
3. Compare the implementation against the agreed scope line by line.
4. Inspect the diff and remove debug artifacts, secrets, unsupported claims, and unused dependencies.
5. Record unverified areas as gaps rather than inferred successes.

