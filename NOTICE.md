# Third-party notices

This repository redistributes modified versions of two MIT-licensed Agent Skills. Both originals permit modification and redistribution under MIT; this file satisfies the "include copyright notice" condition.

## `skills/tdd/`

- **Source:** [mattpocock/skills](https://github.com/mattpocock/skills), path `skills/engineering/tdd/`
- **Pinned at:** tag `v1.3.1`, commit `59db609eb1e18aaf59b63284d0e52255aff0c63c`
- **License:** MIT — Copyright (c) 2026 Matt Pocock
- **Files kept as-is:** `mocking.md`, `tests.md`
- **Modifications to `SKILL.md`:**
  1. Added a time-boxed fallback to the seam-confirmation step — the original requires confirming test seams "with the user" before writing a test; in this exam, no reviewer is available mid-exercise, so the candidate now decides the seam alone after a short wait and records the reason in `DECISIONS.md`, instead of stalling.
  2. Removed the instruction to call the `codebase-design` skill for module-boundary vocabulary (not included in this kit) and replaced it with three inline sentences covering the same decision.
  3. Removed the instruction to defer refactor review to the `code-review` skill (excluded from the real exam per this project's `EXAM-ALLOWLIST.md`) and pointed instead at the diff-review step already required by `fde-workflow`'s `evidence.md`.
- **Why:** both removed cross-references would otherwise ask the agent to invoke a Skill that is not installed in this kit, producing a dead call during a timed exercise.

## `skills/verification-before-completion/`

- **Source:** [obra/superpowers](https://github.com/obra/superpowers), path `skills/verification-before-completion/`
- **Pinned at:** tag `v7.0.1`, commit `2ce8aa15d05bd57213e6f746f953aafb7ded7a8b`
- **License:** MIT — Copyright (c) 2025 Jesse Vincent
- **Modifications:**
  1. Kept the Iron Law, the Gate Function, and one consolidated claim/evidence table.
  2. Removed the "Rationalization Prevention" excuse table and the "Key Patterns" section — both restate the Gate Function's point a second and third time, which costs context without adding a new rule.
  3. Added a closing paragraph naming this harness's actual verification commands (`npm test`, `npm run build`) and where they fit (before `ACCEPTANCE.md`, before any completion claim to the business owner or in the Q&A).
- **Why:** the original is effective but repeats the same instruction three ways; this kit favors the shorter version per the progressive-disclosure principle already used for `fde-workflow` (see this project's `trainer/research/fde-tool-landscape.md`).

## `skills/fde-workflow/`

Original content, authored for this rehearsal kit. Licensed under this repository's own `LICENSE` (MIT). No third-party material.

## Full MIT license text (applies to both sources above)

```
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
