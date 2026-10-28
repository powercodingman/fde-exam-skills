---
name: fde-workflow
description: Run a time-boxed FDE rehearsal when the user asks for an FDE exercise, stakeholder interview, acceptance evidence, or post-submission defense.
---

# FDE workflow

Use this skill at the start of an FDE exercise. Preserve the user's chosen stack, time limit, and environment rules. The goal is one valuable workflow that the candidate can operate, verify, explain, and hand off.

## 1. Discover

Read the assignment and existing workspace evidence. Separate provided facts, stakeholder-confirmed facts, assumptions, and open questions.

Interview the stakeholder before choosing the solution. Read [references/interview.md](references/interview.md) for the question sequence. Record answers in the workspace's interview document as they are confirmed.

Discovery is complete when the current event, workaround, frequency or scale, harm, users, exceptions, and a measurable target are known or explicitly marked unknown.

## 2. Commit

Write a compact agreement covering:

- the problem and affected user;
- current value and target metric;
- the narrow workflow to deliver;
- excluded scope and external dependencies;
- human decision points, sensitive data, and failure recovery;
- the first end-to-end slice and how it will be verified.

Ask the stakeholder to confirm this understanding when the exercise supports follow-up questions. Record consequential choices and rejected alternatives in the decision document.

Commit is complete when each planned feature maps to a confirmed problem or target and the first slice has an observable pass/fail check.

## 3. Deliver

Build the first complete slice through the public interface, then add only the next highest-value slice. Keep business rules in deterministic, testable code. Automated suggestions must expose their reason and remain reviewable by a person when the decision has operational consequences.

Use external Skills, MCP, or public starters only for a named bottleneck. Record each selected or rejected tool in `TOOLING.md`, including evidence, risk, and fallback.

Read [references/evidence.md](references/evidence.md) before claiming a slice or the submission complete. Save failures and the correction that followed; a smooth narrative without observable checks is weak evidence.

Delivery is complete when the agreed workflow runs, fresh tests and build checks have been read, acceptance results match the implementation, and known gaps are explicit.

## 4. Defend and hand off

Freeze the submission before preparing answers. Explain only the frozen code and observed behavior.

Complete the handoff with run instructions, operating assumptions, limits, failure recovery, and the next safe improvement. Read [references/qa-defense.md](references/qa-defense.md) and rehearse answers without AI or copy-paste.

The exercise is complete when every claim in the handoff and answers points to a file, test, command output, decision, or stakeholder fact in the frozen submission.

