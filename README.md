# fde-exam-skills

Three Agent Skills, vetted and pinned for use during a time-boxed FDE (Forward Deployed Engineer) take-home exam (e.g. Cofa Probe). Clone this repo on exam day instead of installing anything live — it exists so no package manager or skill-marketplace network call is required once the exam starts.

## What's inside

| Skill | Source | Status |
|---|---|---|
| `skills/fde-workflow/` | Original (this author) | Router: discover → commit → deliver → defend and hand off |
| `skills/tdd/` | Modified from [mattpocock/skills](https://github.com/mattpocock/skills) `v1.3.1`, MIT | Red-green loop, with exam-safe seam-decision fallback (see `NOTICE.md`) |
| `skills/verification-before-completion/` | Trimmed from [obra/superpowers](https://github.com/obra/superpowers) `v7.0.1`, MIT | Evidence-before-claims gate, shortened |

See `NOTICE.md` for exactly what was changed in the two third-party skills and why — both are included here specifically because the unmodified originals conflict with a timed exam (a skill call to a Skill that isn't installed, or a seam-confirmation step with no one available to confirm with).

## Install during the exam

```bash
git clone --branch v1.0.0 https://github.com/powercodingman/fde-exam-skills.git
```

Then copy (do not symlink, to avoid any write-back into this clone) the three folders under `skills/` into wherever the exam's agent reads skills from, e.g.:

```bash
cp -r fde-exam-skills/skills/fde-workflow .agents/skills/fde-workflow
cp -r fde-exam-skills/skills/tdd .agents/skills/tdd
cp -r fde-exam-skills/skills/verification-before-completion .agents/skills/verification-before-completion
```

Adjust the destination path to whatever the actual exam environment's skill directory turns out to be — confirm this during the pre-exam environment check, not on exam day.

## Before you rely on this on exam day

- **Re-read the pinned commits.** `mattpocock/skills` and `obra/superpowers` can change after this repo was pinned. Re-diff against the pinned tags above before trusting this clone again.
- **Confirm `git clone` of a public repo is actually allowed** under the current exam rules — this repo assumes "public GitHub repo, no personal upload, no `git push` during the exam," per this author's own `trainer/tooling/SELECTION-PROTOCOL.md` §0 gate, not per anything published on the exam platform's own site (its public page states only the "기술·의도·인지" scoring axes and "same environment for everyone," not a tool allowlist).
- **No scripts, no network calls, no write access outside the exam workspace** in any of the three skills — confirmed by reading every file in this repo; re-confirm after any future re-pin.
- **This repo is intentionally public** so it can be cloned without authentication during the exam. It contains no exam-private material — no scenario data, no rubric, no persona script.
