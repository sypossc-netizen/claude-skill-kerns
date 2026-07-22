---
name: kerns
description: >-
  Guide a rotation, course, or curriculum through Kern's six-step model of
  curriculum development, either one step at a time or drafted in full from
  notes the user provides, producing a finished analysis-plan document exported
  to Word. Use whenever the user wants to design, revamp, redesign, or formally
  analyze a residency rotation, medical-student clerkship, lecture series, boot
  camp, fellowship, or any health-professions curriculum — or says "Kern's",
  "curriculum development", "needs assessment", "learning objectives / SMART
  objectives", "EPA / milestone mapping", or is preparing a
  curriculum-development reflection or portfolio piece. Also use to resume,
  review, or continue an in-progress Kern's analysis from existing notes.
  Trigger even when the user names only the rotation ("let's redesign our lab
  medicine rotation") without saying "Kern's" — this is the right tool for
  structured curriculum design.
---

# Kern's Curriculum Analysis

Walk the user through Kern's six-step model of curriculum development and produce a finished, defensible analysis-plan document. Kern's exists to convert curricular change from **reactive → intentional, implicit → explicit, and siloed → aligned** — so the point of this skill is to make each design decision explicit and traceable, not to produce a plausible-looking document fast. A curriculum built without the stakeholders' data is "a rotation on paper."

Full framework reference (the six steps in detail, Bloom's verbs, the SMART objective template, learning theories, competency frameworks, the running-note template, and the Word export recipe) lives in `references/kerns-framework.md`. Read it when you need the specifics; this file is the workflow.

## Core operating principles

These are what make the analysis honest and reusable. Hold them throughout:

1. **Assume the user has never heard of Kern's.** Most people arriving here have a rotation they want to fix, not a curriculum-development vocabulary. Open with the orientation in Step 0a, and introduce every step with a plain-language sentence about what it is for before asking for anything. Terms like "targeted needs assessment," "entrustable professional activity," and "formative versus summative" each need a clause of explanation the first time they appear. A user who already knows the model will tell you to skip ahead; a user who doesn't will otherwise answer questions they don't understand.
2. **Never go hunting through the user's files.** Context comes from what the user hands you — a directory or document they name. Do not scan, grep, or glob for prior analyses, seed material, or literature, and do not read beyond what they pointed at. If you need something, ask. Unprompted searching wastes their time on material they didn't choose and quietly pulls the wrong sources into a document they'll put their name on.
3. **Label everything `[R]` (real) vs `[H]` (hypothetical).** Real = an actual program decision or measured datum. Hypothetical = illustrative, grounded in literature but not yet measured. This lets the user complete a full analysis now for a reflection or portfolio and swap in real data later without the two ever blurring. Never present hypothetical findings as real.
4. **Table-for-later, never confabulate.** Kern's Step 2 demands data (surveys, course reviews, in-training exam scores, milestone data). When the user doesn't have it, do NOT invent findings. Record the *analysis plan* for when the data arrives, put a clearly-labeled `[H]` placeholder in its place, and keep moving. This binds hardest in full-draft mode, where the pressure to fill every section is greatest.
5. **Reverse-map existing changes.** Most real curricula are already mid-revamp. When the user has already made changes, they almost always arrived *strategy-first* (Step 4 before Steps 1–3) — the signature of reactive change. Map each existing change to the Kern's step it implicitly lives in, then retrofit the explicit objective (Step 3) and evaluation hook (Step 6) it was missing. This is usually the highest-value thing the skill does.
6. **Ground claims in real sources.** Build the general needs assessment from the notes and references the user provided. If they gave you none, say plainly that the field-level assessment is unsourced and offer to look something up — never quietly fill it from memory, and never fabricate a citation.
7. **Accrete into one running note.** The working substrate is a single file in the resolved workspace; update it as you go so the analysis survives the conversation and a later session can pick it up.

## Workflow

### Step 0 — Orient, onboard, frame

**0a. Orient the user — always, and first.** Assume they have never heard of Kern's. Before any question, give them a compact map of where this is going. Rephrase freely, but keep it this short — it is a signpost, not a lecture:

> Kern's is the standard six-step model for designing and revising health-professions curricula. The short version:
>
> 1. **Problem identification** — what's actually wrong, and what the wider field says the gap is.
> 2. **Targeted needs assessment** — what's true for *your* learners in *your* setting, established from data rather than impressions.
> 3. **Goals and objectives** — what learners should be able to do, stated specifically enough to measure.
> 4. **Educational strategies** — the teaching methods and content that get them there.
> 5. **Implementation** — the support, resources, faculty preparation, and pilot needed to make it real.
> 6. **Evaluation** — whether it worked, judged for the learners, the faculty, and the curriculum itself. This loops back to step 1.
>
> Where you don't have real data yet, I'll mark a clearly-labeled placeholder rather than invent a finding, so you can swap real numbers in later.

Tell them they can ask what any term means at any point, then go straight to 0b — don't wait for a reply to the orientation.

**0b. Onboard — three questions, asked together.** A single multiple-choice block works well. Skip any question the invocation already answered (`/kerns ~/curricula/clerkship` answers the second).

**Get the curriculum's name as its own plain question.** Do not bundle it into the choice block or tack it onto the prose beside one — a choice block cannot carry free text, so the name falls through and you reach the point of creating files without it. Ask for it directly and wait for it. Everything downstream is named for it: the running note, the exported document, the objectives. The same applies to any other free-text answer you need, notably the existing-changes capture in 0d.

1. **New or existing?** Is this curriculum being analyzed for the first time, or is there a prior Kern's analysis to continue?
2. **Any notes or documents to work from?** Meeting notes, a seminar capture, a prior curriculum document, course reviews, evaluation exports. **The user points you at a path; you never search for it.** If they say there's nothing, that's a valid answer — proceed on what they tell you directly.
3. **How do you want to proceed — stepwise or full draft?** Explain the trade-off in one line each, since the labels mean nothing on their own:
   - **Stepwise** — one step at a time, each settled with you before moving on. Slower, but every decision is yours. Right when there's little written down, or when the thinking is the point.
   - **Full draft** — I read your material and draft all six steps at once, then hand you a list of the gaps to fill. Faster, and better when you have real notes to work from. Recommend this one when they answered question 2 with actual material.

**0c. Resolve the workspace.** Where the running note and the exported document land, in precedence order — an explicit user path always wins:

1. A path the user specified as the destination.
2. When continuing, the directory the existing analysis already lives in.
3. A detected notes vault (e.g. an `.obsidian/` directory at the root) → stage in its inbox/staging folder and honor that vault's conventions (frontmatter schema, staging rules, review-state flags).
4. Otherwise → `./kerns-<curriculum-slug>/` under the current working directory.

State the resolved path and confirm it before writing the first file.

**0d. Frame.** Read whatever material the user pointed to, then establish the four things that shape everything downstream. In full-draft mode, extract what you can from their material and confirm it rather than asking cold:

- **Learner level** — graduate/postgraduate trainees (residents, registrars, fellows: competency frameworks, milestones/EPAs, board or specialty exams) vs undergraduate/pre-licensure students (medical, nursing, pharmacy: programmatic accreditation, faculty-owned curriculum, licensing exams) vs both. This decides which constraints govern.
- **Scope** — which content domains the curriculum covers.
- **Core problem** — graduated-autonomy gap / content coverage and structure / assessment gap / reactive drift. Multi-select; they usually co-occur.
- **Redesign or build?** A redesign of a curriculum that already runs has existing changes to reverse-map and its own course reviews to mine in Step 2. A build of one that doesn't exist yet has neither, and leans on the field-level assessment and comparison programs instead. Ask rather than infer. For a redesign, also capture **existing changes already made**, verbatim — that is the reverse-mapping spine.

Create the running note (see Output) with the framing recorded, then branch on the mode chosen in 0b.

---

### Mode A — Stepwise

Work Steps 1–6 in order, one at a time. For each: give the plain-language lead-in, ask the context questions that step needs, draft it, show the user, refine, write it to the running note, and only then advance. Never present two steps at once, and never move on from a step the user hasn't settled.

### Mode B — Full draft

Read the user's material, then draft all six steps in one pass and write them to the running note. Then **hand back a gap list** — every place you inserted an `[H]` placeholder, every unanswered question, every claim you couldn't source — ranked by how much it matters, and work through it with the user.

Full-draft mode is where confabulation pressure is highest: a six-section document with visible holes looks unfinished, and the temptation is to smooth them over. Don't. An `[H]` placeholder and an honest gap list are the deliverable; invented survey findings are worse than blank sections. If the user's material doesn't establish something, say so in the document itself.

---

### Step 1 — Problem Identification & General Needs Assessment

Two halves. **Problem identification:** define the problem *broadly* — its effect on learners, faculty, patients, the health system, and the field — as a **current-situation vs ideal-situation** statement, plus the **environmental factors** you must design around but can't change (accreditation bodies, licensing and board exams, staffing and turnaround pressure, institutional governance). **General needs assessment:** the field-level ideal-vs-current gap, independent of this institution — ground it in the literature the user provided and label sources `[R]`.

### Step 2 — Targeted Needs Assessment (TNA)

Localize the field gap to *these* learners and *this* environment. Kern's demands data here — decide with the user whether to field new instruments (learner and faculty surveys, split technical vs analytical, plus barriers-to-autonomy) or use **existing data** (prior course reviews, in-training exam scores, milestone or competency-committee data). Build the **stakeholder map** (every program and rotation director, quality officer, coordinator, and the learners). If the data isn't on hand, record the **analysis plan** and insert an `[H]` expected-gap list grounded in the GNA. Produce a **ranked gap list** — this is what Step 3 targets.

### Step 3 — Goals & Objectives

One broad **goal** (longitudinal). Then **SMART objectives** in the form *who will do how much of what by when, assessed how* — Specific, Measurable, Achievable, Relevant, Time-bound. Assign each a **Bloom's level** and make sure the assessment matches that level (a "Create" objective is judged by a produced artifact, not a multiple-choice question). Map each to the program's competency framework — milestones/EPAs, CanMEDS roles, or whatever governs locally. Crucially, **write an objective for each existing change** (the reverse-map) plus objectives for the top TNA gaps. See `references/kerns-framework.md` for the SMART template and Bloom verbs.

### Step 4 — Educational Strategies

Match methods to objectives. A **structural gap needs a structural strategy** (a structured rotation with explicit faculty rules, not "some interesting cases"). For each strategy note the **learning theory** it draws on (behaviorism, cognitivism, social learning, constructivism, multimedia, mastery/deliberate practice) and which objective it serves. Aim for more than one way in per objective. Flag method trade-offs (small-group scales poorly; lectures depend on the faculty member; quizzing needs material and practice).

### Step 5 — Implementation

**Political support** (who owns the curriculum — route to the right committee or associate dean, not the top of the org chart), **resources** (people, materials, space, funding), **faculty development** (the make-or-break — calibrate any entrustment or assessment tool against an *ideal* scenario; borrow national training modules rather than building your own; protect standing faculty time), a **pilot** before full rollout, and a **scholarship hook** (document the process to publish). Capture the sequence: Admin → Resources → Support → Pilot → Implementation.

### Step 6 — Evaluation & Feedback

Three layers: **learner** outcomes, **faculty** behavior change, and the **curriculum itself** as a continuous-improvement project (Step 6 loops back to Step 1). For each, name the metric and instrument and whether it's formative (during, to improve) or summative (at the end, to judge) — formative before summative. Address **response rate** and **validity** (attitude / history / instrumentation / implementation). Add **curriculum maintenance** — design it to survive change ("can it run two faculty short?") and set the next iteration's evaluation plan *before* the pilot ends.

### Step 7 — Output

The default deliverable is a **Word document** in the workspace resolved at 0c. Produce it without being asked; confirm only the destination.

- **Word `.doc`** — the analysis rendered clean for an outside reader (a committee, a program director, a portfolio reviewer): numbered 1–6 with sub-numbering (1.1, 1.2, …), an `[R]`/`[H]` legend at the top, and the working scaffolding (status parentheticals, `## Next`) dropped. Derive it from the running note; never re-draft the analysis from scratch. Follow the export recipe in `references/kerns-framework.md` — **write to local scratch first, then `cp` into the destination**, because sandboxed writes silently fail to reach cloud-sync and network mounts, and verify the landed file with `ls -la` rather than trusting a success message.
- **Running analysis note** — always kept alongside it, as the editable substrate and the resume point.
- **Reflection** (optional) — a first-person portfolio or certificate reflection derived from the analysis, if the user is in an educator-development program. Align it to the program's actual prompt and rubric; ask for those if the user mentions a program but hasn't supplied them.

## Output: the running note

Stage a single markdown file in the resolved workspace, named for the curriculum (e.g. `<Curriculum Name> - Kerns Analysis.md`). Structure it as the six steps with `[R]`/`[H]` labels, a reverse-mapping table for existing changes, and a `## Next` section listing what's tabled (data to collect) and what's next. See `references/kerns-framework.md` for the full note template and frontmatter schema.

Update it as you go rather than only at the end — it is the durable substrate, it lets a later session resume, and it is what the Word export is derived from.

## Guardrails

- **No confabulated data or citations.** If a needs-assessment finding, statistic, or source isn't real and on hand, mark it `[H]` or ask. This is non-negotiable — a curriculum defended to a committee on invented survey data is worse than no analysis.
- **Never search the user's files unprompted.** They point; you read. See principle 2.
- **Honor the workspace's conventions** when one exists (staging rules, frontmatter schemas, naming rules). Don't edit canonical or published notes without explicit instruction — stage instead.
- **Never set a review-approval flag yourself.** If the workspace uses one (`user_reviewed`, `state: canonical`, or similar), that field belongs to the user; leave staged work marked unreviewed and say so.
- **Treat the running note as append-mostly.** Edit the sections you are working on; don't regenerate the whole file. A resumed analysis may contain real decisions and real data from sessions you have no record of.
- **Deliverables go where the user specifies.** An explicit path is the user's override of any default location.

## Resuming an existing analysis

When the user chose "existing" at 0b, read the prior analysis end to end, then show a step-completion table: for each of Steps 1–6, is it Complete `[R]`, Complete `[H]` (placeholder awaiting real data), Partial, or Absent? Include open items from its `## Next` section, and confirm the resume point rather than assuming the first gap is where they want to work.

**When the prior material doesn't match this skill's template** — it predates the skill, came from another tool, or is raw notes or a Word export — don't force it into the template silently. Read it, infer which steps its content maps onto, and present that mapping as a *proposal* for the user to correct. Then ask whether to migrate it into a fresh running note (keeping the original untouched as the source) or work in place. Migration is usually right, but it's the user's call — the original may be a shared or submitted document.

Resume safety rules:

- **Never silently redo a settled step.** Prior decisions are the user's, not yours to relitigate.
- **Never overwrite `[R]` content with `[H]` content.** Real data replaces hypothetical, never the reverse.
- **Never bulk-rewrite the running note.** It is a multi-session accretion and may hold work you never saw. Make targeted edits to the sections you're changing. If a restructure really is needed, say what you intend to change and get the user's go-ahead first — and where the file isn't under version control, copy it aside before the rewrite.
