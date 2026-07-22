# kerns — a Claude Code skill for curriculum development

A [Claude Code](https://claude.com/claude-code) skill that walks a rotation, course, or curriculum through **Kern's six-step model of curriculum development**, either one step at a time or drafted in full from your own notes, and produces a finished, defensible analysis-plan document.

Built for graduate and undergraduate medical education — residency rotations, clerkships, lecture series, boot camps, fellowships — but the workflow applies to any structured health-professions curriculum.

## What it does

Kern's six-step model exists to convert curricular change from **reactive → intentional, implicit → explicit, and siloed → aligned**. This skill enforces that discipline rather than producing a plausible-looking document fast:

1. **Problem Identification & General Needs Assessment** — current vs. ideal at the field level, plus the environmental factors you must design around.
2. **Targeted Needs Assessment** — localize the field gap to *your* learners and environment; build a stakeholder map and a ranked gap list.
3. **Goals & Objectives** — one broad goal, then SMART objectives with Bloom's levels, mapped to whichever competency framework governs your program.
4. **Educational Strategies** — match methods to objectives, each grounded in a named learning theory.
5. **Implementation** — political support, resources, faculty development, pilot, scholarship hook.
6. **Evaluation & Feedback** — learner, faculty, and curriculum-as-continuous-improvement layers; validity and response rate; curriculum maintenance.

## How a session goes

It opens with a short plain-language map of the six steps — the skill assumes you have never heard of Kern's, and explains each term the first time it appears. Then three questions:

- **New or existing?** Starting fresh, or continuing a prior analysis.
- **Any notes to work from?** You point at a file or folder. **The skill never searches your filesystem** — it reads what you name and nothing else.
- **Stepwise or full draft?** Stepwise settles each step with you before advancing. Full draft reads your material, writes all six steps in one pass, then hands you a ranked list of the gaps to fill.

From there it frames the curriculum — learner level, scope, core problem, and whether this is a redesign of something already running or a build of something new — and works through the steps. The output is a Word document, with an editable markdown note kept alongside it as the working substrate and resume point.

### Design choices worth knowing about

- **Assumes no prior knowledge.** Curriculum-development vocabulary gets explained rather than assumed. Most people arrive with a rotation they want to fix, not a familiarity with Kern's.
- **Never searches your files.** Context comes only from what you hand it. Unprompted searching spends your time on material you didn't choose and quietly pulls unvetted sources into a document you'll put your name on.
- **`[R]` real vs. `[H]` hypothetical labeling.** Every finding is tagged. You can complete a full analysis today for a portfolio or reflection, then swap in real survey data later without the two ever blurring.
- **Never confabulates data.** Kern's Step 2 demands real data. When you don't have it, the skill records the *analysis plan* for when the data arrives and inserts a clearly-labeled placeholder — it does not invent survey findings, statistics, or citations. A curriculum defended to a committee on invented data is worse than no analysis. This binds hardest in full-draft mode, where a six-section document with visible holes looks unfinished and the pull to smooth them over is strongest.
- **Reverse-maps existing changes.** Most real curricula are already mid-revamp, and those changes almost always arrived strategy-first (Step 4 before Steps 1–3) — the signature of reactive change. The skill maps each existing change to the step it implicitly lives in, then retrofits the explicit objective and evaluation hook it was missing. This is usually the highest-value thing it does.
- **Safe to resume.** A later session maps which steps are complete before editing anything, won't overwrite real data with placeholders, and won't bulk-rewrite a note that may hold work from sessions it never saw.

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

Point it at material up front if you have some:

```
/kerns ~/curricula/lab-medicine-rotation
```

Or just describe the work — the skill triggers on curriculum-design intent even when you don't name Kern's:

> let's redesign our lab medicine rotation

> I need to do a needs assessment for the hematopathology rotation

> help me write SMART objectives mapped to our milestones

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | The workflow — operating principles, Step 0 onboarding, the two modes, Steps 1–7, output format, guardrails, resume rules. |
| `references/kerns-framework.md` | The reference — six steps in detail, SMART template, Bloom's verbs, learning theories, competency frameworks, reverse-mapping pattern, running-note template, Word export recipe. Loaded on demand. |

## Notes

- **Not tied to any one country or specialty.** ACGME milestones and EPAs sit alongside CanMEDS, the UK GMC framework, and AACN Essentials; the skill asks which framework governs your program rather than assuming one. In-training exams are treated the same way.
- **Not tied to any note-taking setup.** If you work in an Obsidian vault it stages notes there and honors the vault's conventions; otherwise it writes to a path you name or a folder in the working directory.
- The framework is based on Kern's *Curriculum Development for Medical Education: A Six-Step Approach*, the standard text in health-professions-education programs. This repo contains an original workflow implementation, not the book's content.

## License

MIT — see [LICENSE](LICENSE).
