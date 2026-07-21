---
name: kerns
description: >-
  Guide a rotation, course, or curriculum through Kern's six-step model of
  curriculum development as an interactive, one-step-at-a-time back-and-forth,
  producing a finished analysis-plan document. Use whenever the user wants to
  design, revamp, redesign, or formally analyze a residency rotation, medical-
  student clerkship, lecture series, boot camp, or any GME/UME curriculum — or
  says "Kern's", "curriculum development", "needs assessment", "learning
  objectives / SMART objectives", "EPA / milestone mapping", or is preparing a
  curriculum-development reflection or portfolio piece. Trigger even when the
  user names only the rotation ("let's redesign our lab medicine rotation")
  without saying "Kern's" — this is the right tool for structured curriculum
  design.
---

# Kern's Curriculum Analysis

Walk the user through Kern's six-step model of curriculum development, one step at a time, and accrete the result into a finished, defensible analysis-plan document. Kern's exists to convert curricular change from **reactive → intentional, implicit → explicit, and siloed → aligned** — so the whole point of this skill is to make each design decision explicit and traceable, not to produce a plausible-looking document fast. Move deliberately and get the user's input at each step; a curriculum built without the stakeholders' data is "a rotation on paper."

Full framework reference (the six steps in detail, Bloom's verbs, the SMART objective template, learning theories, ACGME competency abbreviations, and the Word/Drive export recipe) lives in `references/kerns-framework.md`. Read it when you need the specifics; this file is the workflow.

## Core operating principles

These are what make the analysis honest and reusable. Hold them throughout:

1. **One step at a time.** Never dump all six steps. Present a step, settle it with the user, then advance. The user asked to "go through" Kern's — respect that rhythm.
2. **Label everything `[R]` (real) vs `[H]` (hypothetical).** Real = an actual program decision or measured datum. Hypothetical = illustrative, grounded in literature but not yet measured. This lets the user complete a full analysis now for a reflection/portfolio and swap in real data later without the two ever blurring. Never present hypothetical findings as real.
3. **Table-for-later, never confabulate.** Kern's Step 2 demands data (surveys, course reviews, RISE/in-service scores, milestone data). When the user doesn't have it on hand, do NOT invent findings. Record the *analysis plan* for when the data arrives, put a clearly-labeled `[H]` placeholder in its place, and keep moving.
4. **Reverse-map existing changes.** Most real curricula are already mid-revamp. When the user has already made changes, they almost always arrived *strategy-first* (Step 4 before Steps 1–3) — the signature of reactive change. Map each existing change to the Kern's step it implicitly lives in, then retrofit the explicit objective (Step 3) and evaluation hook (Step 6) it was missing. This is usually the highest-value thing the skill does.
5. **Ground the general needs assessment in what's already known.** Pull the field-level ideal-vs-current from existing literature/notes the user has (search their vault/library first) rather than a cold web crawl. Cite it.
6. **Accrete into one running note, not just chat.** The working substrate is a single staging note; update it after each step so the analysis survives the conversation.

## Workflow

### Step 0 — Intake and framing

Read any seed material the user points to (a seminar note, prior-meeting notes, an existing curriculum project). If the work touches an Obsidian Research vault, honor its preflight and stage the running note in `_inbox/` per vault rules.

Then get the framing that shapes everything downstream. Ask these as a small, focused set (a multiple-choice question block works well) — don't interrogate:

- **Learner level:** GME residents (ACGME milestones/EPAs, board exam, competency-based) vs UME students (LCME, faculty own the curriculum, USMLE) vs both. This decides which constraints govern.
- **Scope:** which content domains the rotation/course covers.
- **Core problem driving the work:** graduated-autonomy gap / content coverage & structure / assessment gap / reactive drift (multi-select — they often co-occur).
- **Existing changes already made** (free text): capture these verbatim; they become the reverse-mapping spine.

Create the running note (see Output) with the framing recorded.

### Step 1 — Problem Identification & General Needs Assessment

Two halves. **Problem identification:** define the problem *broadly* — its effect on learners, faculty, patients, the health system, and the field — as a **current-situation vs ideal-situation** statement, plus the **environmental factors** you must design around but can't change (accreditation bodies, board exams, staffing/turnaround pressure, institutional governance). **General needs assessment:** the field-level ideal-vs-current gap, independent of this institution — ground it in existing literature and label sources `[R]`.

Draft it, show the user, refine. Write to the note.

### Step 2 — Targeted Needs Assessment (TNA)

Localize the field gap to *these* learners and *this* environment. "Kern's demands data" — decide with the user whether to field new instruments (resident + faculty surveys, split technical vs analytical, plus barriers-to-autonomy) or use **existing data** (prior course reviews, in-service/RISE scores, milestone data). Build the **stakeholder map** (every director, quality officer, coordinator, and the learners). If the data isn't on hand, record the **analysis plan** and insert an `[H]` expected-gap list grounded in the GNA. Produce a **ranked gap list** — this is what Step 3 targets.

### Step 3 — Goals & Objectives

One broad **goal** (longitudinal). Then **SMART objectives** in the form *who will do how much of what by when, assessed how* — Specific, Measurable, Achievable, Relevant, Time-bound. Assign each a **Bloom's level** and make sure the assessment matches that level (a "Create" objective is judged by a produced artifact, not an MCQ). Map each to **milestones/EPAs**. Crucially, **write an objective for each existing change** (the reverse-map) plus objectives for the top TNA gaps. See `references/kerns-framework.md` for the SMART template and Bloom verbs.

### Step 4 — Educational Strategies

Match methods to objectives. A **structural gap needs a structural strategy** (a structured rotation with explicit faculty rules, not "some interesting cases"). For each strategy note the **learning theory** it draws on (behaviorism, cognitivism, social learning, constructivism, multimedia, mastery/deliberate practice) and which objective it serves. Aim for multimedia coverage — more than one way in per objective. Flag method trade-offs (small-group scales poorly; lectures depend on the faculty member; quizzing needs material + practice).

### Step 5 — Implementation

**Political support** (who owns the curriculum — route to the right committee/dean, not the top of the org chart), **resources** (people, materials, space, funding), **faculty development** (the make-or-break — calibrate any entrustment/EPA tool against an *ideal* scenario; borrow national training modules rather than building your own; protect standing faculty time), a **pilot** before full rollout, and a **scholarship hook** (document the process to publish). Capture the sequence: Admin → Resources → Support → Pilot → Implementation.

### Step 6 — Evaluation & Feedback

Three layers: **learner** outcomes, **faculty** behavior change, and the **curriculum itself** as a CQI project (Step 6 loops back to Step 1). For each, name the metric and instrument and whether it's formative or summative (formative before summative). Address **response rate** and **validity** (attitude / history / instrumentation / implementation). Add **curriculum maintenance** — design it to survive change ("can it run two faculty short?") and set the next iteration's evaluation plan *before* the pilot ends.

### Step 7 — Output

Assemble the finished deliverable and confirm format/destination with the user:

- **Running analysis note** — always; the accreted `_inbox/` note.
- **Structured analysis-plan document** — the clean numbered 1–6 layout (sub-numbered 1.1, 1.2, …), `[R]`/`[H]` legend at top.
- **Reflection** (optional) — a first-person portfolio/certificate reflection derived from the analysis, if the user is in an educator-development program. Align it to the program's actual prompt + rubric if those files exist.
- **Export** (optional) — Word `.doc` to a user-specified folder. See the export recipe in `references/kerns-framework.md` — **write to local scratch first, then `cp` into the destination**, because sandboxed writes silently fail to reach Google Drive / network FUSE mounts.

## Output: the running note

Stage a single note (in an Obsidian vault: `_inbox/<Name> - Kerns Redesign.md`, `state: draft`, `user_reviewed: false`, complete frontmatter). Structure it as the six steps with the `[R]`/`[H]` labels, a reverse-mapping table for existing changes, and a `## Next` section listing what's tabled (data to collect) and what's next. Update it after each step rather than only at the end — it is the durable substrate, and it lets the user promote the analysis to canonical when ready. Never set `user_reviewed` yourself.

## Guardrails

- **No confabulated data or citations.** If a needs-assessment finding, statistic, or source isn't real and on hand, mark it `[H]` or ask. This is non-negotiable — a curriculum defended to a committee on invented survey data is worse than no analysis.
- **Honor vault conventions** when operating in a Research vault (preflight, staging, frontmatter); don't edit canonical notes without explicit instruction.
- **Drive/Office deliverables** go where the user specifies; an explicit path is the user's override of any default location.
