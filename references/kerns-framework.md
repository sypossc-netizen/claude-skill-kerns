# Kern's Framework — Reference

Detailed reference for the `/kerns` skill. Load when you need the specifics of a step, the objective/verb templates, the running-note template, or the export recipe.

## Contents
1. The six steps in detail
2. SMART objective template
3. Bloom's taxonomy verbs (match assessment to level)
4. Learning theories (Step 4)
5. Competency frameworks and assessment vocabulary
6. Reverse-mapping pattern (existing changes → Kern's slots)
7. Running-note template and frontmatter
8. Word `.doc` export recipe (cloud-sync-safe)

---

## 1. The six steps in detail

Kern's *Curriculum Development for Medical Education* — the standard text in health-professions-education programs. The six steps are a **loop**; every step cross-talks with the others, so a change in one domain affects the rest.

1. **Problem Identification & General Needs Assessment (GNA)**
   - Define the problem *broadly*: effect on learners, faculty, patients, health systems, society.
   - Current situation vs ideal situation vs environmental factors (people, methods).
   - Environmental factors you can't change but must design around: accreditation bodies, licensing and board exams, institutional and postgraduate-training governance.
   - Stakeholders, focus groups.

2. **Targeted Needs Assessment (TNA)**
   - Apply the GNA to *your* specific learners and environment.
   - Build stakeholder relationships; identify learners; map the learning environment (course and rotation directors, faculty, competency/evaluation committees).
   - Methods: surveys, interviews, focus groups — or existing data (course reviews, in-training/in-service exam scores, milestone data).
   - Expect learners and faculty to disagree; the perception gap is itself a finding.

3. **Goals & Objectives**
   - Goals: broad, longitudinal.
   - Objectives: narrow, SMART; "who will do how much of what by when."
   - Map to the local competency framework; competency-based, not time-based.

4. **Educational Strategies (methods + content)**
   - Match verbs to Bloom's; assessment must match the cognitive level taught.
   - A structural gap needs a structural strategy.
   - Method trade-offs: textbooks (cheap, need motivation); video (complex items, screen fatigue); lectures (scale, quality varies); test-enhanced quizzing (needs practice); small-group (rich feedback, caps ~8/faculty).

5. **Implementation**
   - Political support: faculty own the curriculum — route to the right committee or associate dean, not the top of the org chart.
   - Resources = people, materials, funding, space.
   - Document the change → scholarship. Run a pilot first.
   - Sequence: Admin → Resources → Support → Pilot → Implementation.

6. **Evaluation & Feedback**
   - Levels: individual learner vs program/course vs faculty.
   - Response rate matters; choose instrument by ease of collection; account for cohort attitudes/history/bias.
   - Validity across Attitude, History, Implementation, Instrumentation.
   - Formative (during) before summative; qualitative thematically, quantitative statistically.
   - *Curriculum maintenance:* plan for constant change (accreditation, institution, faculty attrition) — "can it run two faculty short?" Set the next evaluation plan before the pilot ends.

---

## 2. SMART objective template

> By [when], [who] will [Bloom verb] [how much of what] to [measurable standard], assessed by [instrument].

- **S**pecific — one behavior, unambiguous.
- **M**easurable — a number or clear threshold (e.g., ≥70% accuracy, entrustment ≥4).
- **A**chievable — realistic for the learner level and timeframe.
- **R**elevant — traces to a TNA gap or an existing change.
- **T**ime-bound — a deadline (by end of rotation, within 6 months, before graduation).

Assessment must match the Bloom level: a **Create** objective is judged by a produced artifact (a validation, a project), not a multiple-choice question; an **Analyze** objective is fine to assess by case-based MCQ/oral.

---

## 3. Bloom's taxonomy verbs

Remember → Understand → Apply → Analyze → Evaluate → Create.

| Level | Sample verbs |
|---|---|
| Remember | define, list, recall, name, identify |
| Understand | describe, explain, summarize, classify |
| Apply | use, perform, demonstrate, implement, calculate |
| Analyze | analyze, interpret, differentiate, troubleshoot, compare |
| Evaluate | evaluate, judge, critique, justify, prioritize |
| Create | design, construct, develop, produce, validate, author |

---

## 4. Learning theories (Step 4)

- **Behaviorism** — skills, stimulus/response, feedback loops.
- **Cognitivism** — information processing, schema building.
- **Social learning** — group learning, modeling, near-peer teaching.
- **Constructivism** — authentic tasks; learner builds understanding by doing.
- **Multimedia theory** — give more than one way in (text + video + lecture + discussion + assessment).
- **Mastery / deliberate practice** — push into the zone of proximal development; graduated, longitudinal repetition.

---

## 5. Competency frameworks and assessment vocabulary

Ask which framework governs the user's program rather than assuming — objectives in Step 3 must map to *their* framework. Common ones:

**ACGME core competencies** (US graduate medical education):

| Abbrev | Competency |
|---|---|
| PC | Patient Care |
| MK | Medical Knowledge |
| SBP | Systems-Based Practice (includes quality/QI/stewardship) |
| PBLI | Practice-Based Learning & Improvement |
| ICS | Interpersonal & Communication Skills |
| Prof | Professionalism |

**Other frameworks you may encounter:** CanMEDS roles (Canada — Medical Expert, Communicator, Collaborator, Leader, Health Advocate, Scholar, Professional); the UK GMC *Good Medical Practice* domains and specialty curricula; AACN Essentials (US nursing); country- or profession-specific equivalents. Undergraduate/pre-licensure programs typically map to programmatic accreditation standards and licensing-exam blueprints instead.

**EPAs (Entrustable Professional Activities)** rate real-world tasks on an entrustment scale (roughly: 1 = observe only → 5 = able to supervise others / unsupervised practice). Calibrate against an *ideal* entrustment scenario to resolve the common "nobody wants to give a 5 because there's rarely a truly unsupervised opportunity" problem.

**In-training exams** are the usual objective baseline for a TNA and a ready-made pre/post outcome for Step 6. Every specialty has its own (ABIM ITE, RISE in pathology, ABSITE in surgery, and so on) — ask which one applies and whether subscore-level data is available, since a subscore matched to the rotation's domain is far more useful than a composite.

---

## 6. Reverse-mapping pattern

When the user has already made changes (the usual case for a rotation "revamp already in progress"), those changes almost always arrived as **strategies without stated objectives** — Step 4 before Steps 1–3. Don't discard them; make them explicit. For each existing change, fill:

| Change | Kern's step it lives in | Implied objective (Step 3 — make explicit) | Evaluation hook (Step 6 — attach) |
|---|---|---|---|

Then in Step 3, write a real SMART objective for each, and in Step 6, a real metric. This converts good instincts into a defensible, aligned curriculum and is typically the highest-value output of the analysis.

---

## 7. Running-note template and frontmatter

One file, accreted across the session and across sessions. Name it for the curriculum — `<Curriculum Name> - Kerns Analysis.md` — with no dates in the filename (the frontmatter carries those).

**Frontmatter.** If the workspace is a notes vault with its own schema, follow that schema instead and add the Kern's-specific keys to it. Otherwise use this portable minimum:

```yaml
---
title: <Curriculum Name> — Kern's Analysis
note_type: curriculum_analysis
state: draft
learner_level: <GME | UME | both | other>
framework: <ACGME | CanMEDS | GMC | other>
stakeholders: []
phase: <framing | steps_1_2 | steps_3_4 | steps_5_6 | complete_pending_real_data | complete>
last_updated: "YYYY-MM-DD"
---
```

Keep `phase:` current — it is what a later session's Step 0e reads first.

**Body structure:**

```markdown
# <Curriculum Name> — Kern's Analysis

> **Legend:** `[R]` = real (an actual program decision or measured datum) · `[H]` = hypothetical (illustrative, grounded in literature, not yet measured)

<One-paragraph framing: learners, scope, core problem, seed material.>

## Changes already made
<Verbatim capture of what the program has already changed, plus the reverse-mapping table from §6.>

## Kern's Step 1 — Problem Identification & General Needs Assessment
## Kern's Step 2 — Targeted Needs Assessment
## Kern's Step 3 — Goals & Objectives
## Kern's Step 4 — Educational Strategies
## Kern's Step 5 — Implementation
## Kern's Step 6 — Evaluation & Feedback

## Next
- [ ] <Tabled data to collect — what, from whom, and which `[H]` placeholder it replaces>
- [ ] <Next action>
```

Mark each step heading with a parenthetical status when it isn't settled — *(provisional — pending X)*, *(blocked on existing data)*, *(hypothetical worked example)*. That parenthetical plus the `[R]`/`[H]` labels is what makes a resumed session able to tell finished work from placeholder without re-reading everything.

---

## 8. Word `.doc` export recipe (cloud-sync-safe)

No pandoc/LibreOffice is needed. A `.doc` file whose contents are well-formed HTML opens natively in Word and Google Docs, with headings, bold, and tables rendered as real formatting (and no markdown hashmarks). Steps:

1. Compose the document as an HTML file (`<html>…<head><style>…</style></head><body>…</body></html>`). Use `<h1>/<h2>/<h3>`, `<table>`, `<ul>`, `<blockquote>`; inline the CSS in `<head>`. Give it a `.doc` extension.
2. **Write it to local scratch first** — not directly to the destination. Sandboxed file writes silently fail to reach cloud-sync and network mounts (Google Drive, OneDrive, Dropbox, SMB/NFS); the write tool may even report success while nothing lands.
3. **Copy into the destination via shell**, disabling the sandbox for that copy if the destination is a synced or network mount:
   ```bash
   cp "<scratch>/<file>.doc" "<destination folder>/<file>.doc"
   ```
   Then `ls -la` the destination to confirm the byte size — don't trust a "created successfully" message alone.
4. Cloud mounts differ by platform: on macOS, Google Drive lives under `~/Library/CloudStorage/GoogleDrive-<account>/My Drive/…` (a `~/My Drive` path is usually a symlink to the same mount); on Windows it is typically a drive letter such as `G:\My Drive\`. Ask the user for the destination rather than guessing.

Suggested inline stylesheet (clean, prints well, theme-neutral):
```css
body { font-family: Calibri, Arial, sans-serif; font-size: 11pt; line-height: 1.35; }
h1 { font-size: 18pt; color: #1F3864; }
h2 { font-size: 14pt; color: #2E5496; border-bottom: 1px solid #B4C6E7; padding-bottom: 2pt; }
h3 { font-size: 12pt; color: #2E5496; }
table { border-collapse: collapse; width: 100%; font-size: 10pt; }
th { background: #2E5496; color: #fff; text-align: left; padding: 4pt 6pt; border: 1px solid #8EAADB; }
td { padding: 4pt 6pt; border: 1px solid #8EAADB; vertical-align: top; }
blockquote { border-left: 3px solid #B4C6E7; margin-left: 0; padding-left: 12pt; }
```
