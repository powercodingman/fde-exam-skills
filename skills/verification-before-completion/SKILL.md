---
name: verification-before-completion
description: Use when about to claim work is complete, fixed, or passing, before committing or creating PRs - requires running verification commands and confirming output before making any success claims; evidence before assertions always
---

# Verification Before Completion

> Trimmed from [obra/superpowers](https://github.com/obra/superpowers) (MIT, Copyright Jesse Vincent), pinned at tag `v7.0.1` / commit `2ce8aa15d05bd57213e6f746f953aafb7ded7a8b`. See [NOTICE.md](../../NOTICE.md) for what was cut and why.

**Core principle:** Evidence before claims, always.

## The Iron Law

```
NO COMPLETION CLAIMS WITHOUT FRESH VERIFICATION EVIDENCE
```

If you haven't run the verification command in this message, you cannot claim it passes.

## The Gate Function

```
BEFORE claiming any status or expressing satisfaction:

1. IDENTIFY: What command proves this claim?
2. RUN: Execute the FULL command (fresh, complete)
3. READ: Full output, check exit code, count failures
4. VERIFY: Does output confirm the claim?
   - If NO: State actual status with evidence
   - If YES: State claim WITH evidence
5. ONLY THEN: Make the claim

Skip any step = lying, not verifying
```

## Common Failures

| Claim | Requires | Not Sufficient |
|-------|----------|----------------|
| Tests pass | Test command output: 0 failures | Previous run, "should pass" |
| Build succeeds | Build command: exit 0 | Linter passing, logs look good |
| Bug fixed | Test original symptom: passes | Code changed, assumed fixed |
| Requirements met | Line-by-line checklist | Tests passing |
| Agent completed | VCS diff shows changes | Agent reports "success" |

## Red Flags - Stop

- Using "should", "probably", "seems to"
- Expressing satisfaction before verification ("Great!", "Perfect!", "Done!")
- About to commit/push without verification
- Trusting an agent's success report without checking the diff yourself
- Relying on a partial check instead of the full command

## In this exercise

The verification commands are `npm test` and `npm run build` inside the candidate workspace. Run both fresh — and read their actual exit codes and output — before writing `ACCEPTANCE.md`, and before telling the business owner or the post-submission Q&A that anything works. This gate is for the candidate's own in-progress claims; it does not replace `ACCEPTANCE.md`, `evidence.md`'s pre-submission checklist, or the frozen submission's test/build evidence.
