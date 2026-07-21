# kerns — a Claude Code skill for curriculum development

A [Claude Code](https://claude.com/claude-code) skill that walks a rotation, course, or curriculum through **Kern's six-step model of curriculum development** as an interactive, one-step-at-a-time conversation, accreting the result into a finished, defensible analysis-plan document.

Built for graduate and undergraduate medical education — residency rotations, clerkships, lecture series, boot camps — but the workflow applies to any structured curriculum design.

## What it does

Kern's six-step model exists to convert curricular change from **reactive → intentional, implicit → explicit, and siloed → aligned**. This skill enforces that discipline rather than producing a plausible-looking document fast:

1. **Problem Identification & General Needs Assessment** — current vs. ideal at the field level, plus the environmental factors you must design around.
2. **Targeted Needs Assessment** — localize the field gap to *your* learners and environment; build a stakeholder map and a ranked gap list.
3. **Goals & Objectives** — one broad goal, then SMART objectives with Bloom's levels and milestone/EPA mapping.
4. **Educational Strategies** — match methods to objectives, each grounded in a named learning theory.
5. **Implementation** — political support, resources, faculty development, pilot, scholarship hook.
6. **Evaluation & Feedback** — learner, faculty, and curriculum-as-CQI layers; validity and response rate; curriculum maintenance.

### Design choices worth knowing about

- **One step at a time.** The skill never dumps all six steps. It settles each step with you before advancing.
- **`[R]` real vs. `[H]` hypothetical labeling.** Every finding is tagged. You can complete a full analysis today for a portfolio or reflection, then swap in real survey data later without the two ever blurring.
- **Never confabulates data.** Kern's Step 2 demands real data. When you don't have it, the skill records the *analysis plan* for when the data arrives and inserts a clearly-labeled placeholder — it does not invent survey findings, statistics, or citations. A curriculum defended to a committee on invented data is worse than no analysis.
- **Reverse-maps existing changes.** Most real curricula are already mid-revamp, and those changes almost always arrived strategy-first (Step 4 before Steps 1–3) — the signature of reactive change. The skill maps each existing change to the step it implicitly lives in, then retrofits the explicit objective and evaluation hook it was missing. This is usually the highest-value thing it does.
- **Accretes into one running note.** The analysis survives the conversation rather than living only in chat.

## Install

Clone into your Claude Code skills directory:

```bash
git clone https://github.com/sypossc-netizen/claude-skill-kerns.git ~/.claude/skills/kerns
```

Or copy the files manually:

```
~/.claude/skills/kerns/
├── SKILL.md
└── references/
    └── kerns-framework.md
```

Restart Claude Code (or start a new session) and the skill will be available.

## Use

Invoke it directly:

```
/kerns
```

Or just describe the work — the skill triggers on curriculum-design intent even when you don't name Kern's:

> let's redesign our lab medicine rotation

> I need to do a needs assessment for the hematopathology rotation

> help me write SMART objectives mapped to ACGME milestones

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | The workflow — operating principles, Steps 0–7, output format, guardrails. |
| `references/kerns-framework.md` | The reference — six steps in detail, SMART template, Bloom's verbs, learning theories, ACGME competencies, reverse-mapping pattern, Word/Drive export recipe. Loaded on demand. |

## Notes

- Some steps reference an Obsidian vault for staging the running note. That's optional — the skill honors vault conventions when one is present and works fine without.
- The framework is based on Kern's *Curriculum Development for Medical Education: A Six-Step Approach*, the standard text in health-professions-education programs. This repo contains an original workflow implementation, not the book's content.

## License

MIT — see [LICENSE](LICENSE).
