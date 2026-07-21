# Kern's Framework — Reference

Detailed reference for the `/kerns` skill. Load when you need the specifics of a step, the objective/verb templates, or the export recipe.

## Contents
1. The six steps in detail
2. SMART objective template
3. Bloom's taxonomy verbs (match assessment to level)
4. Learning theories (Step 4)
5. ACGME core competencies + abbreviations
6. Reverse-mapping pattern (existing changes → Kern's slots)
7. Word `.doc` export recipe (Drive-safe)

---

## 1. The six steps in detail

Kern's *Curriculum Development for Medical Education* — the standard text in health-professions-education programs. The six steps are a **loop**; every step cross-talks with the others, so a change in one domain affects the rest.

1. **Problem Identification & General Needs Assessment (GNA)**
   - Define the problem *broadly*: effect on learners, faculty, patients, health systems, society.
   - Current situation vs ideal situation vs environmental factors (people, methods).
   - Environmental factors you can't change but must design around: accreditation (LCME/ACGME), board exams (USMLE/ABPath), GME/institutional governance.
   - Stakeholders, focus groups.

2. **Targeted Needs Assessment (TNA)**
   - Apply the GNA to *your* specific learners and environment.
   - Build stakeholder relationships; identify learners; map the learning environment (course/rotation directors, faculty, CCC, PEC).
   - Methods: surveys, interviews, focus groups — or existing data (course reviews, in-service/RISE scores, milestone data).
   - Expect residents and faculty to disagree; the perception gap is itself a finding.

3. **Goals & Objectives**
   - Goals: broad, longitudinal.
   - Objectives: narrow, SMART; "who will do how much of what by when."
   - Map to milestones/EPAs; competency-based, not time-based.

4. **Educational Strategies (methods + content)**
   - Match verbs to Bloom's; assessment must match the cognitive level taught.
   - A structural gap needs a structural strategy.
   - Method trade-offs: textbooks (cheap, need motivation); video (complex items, screen fatigue); lectures (scale, quality varies); test-enhanced quizzing (needs practice); small-group (rich feedback, caps ~8/faculty).

5. **Implementation**
   - Political support: faculty own the curriculum — route to the right committee/associate dean, not the top of the org chart.
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

## 5. ACGME core competencies

| Abbrev | Competency |
|---|---|
| PC | Patient Care |
| MK | Medical Knowledge |
| SBP | Systems-Based Practice (includes quality/QI/stewardship) |
| PBLI | Practice-Based Learning & Improvement |
| ICS | Interpersonal & Communication Skills |
| Prof | Professionalism |

EPAs (Entrustable Professional Activities) rate real-world tasks on an entrustment scale (roughly: 1 = observe only → 5 = able to supervise others / unsupervised practice). Calibrate against an *ideal* entrustment scenario to resolve the common "nobody wants to give a 5 because there's rarely a truly unsupervised opportunity" problem.

---

## 6. Reverse-mapping pattern

When the user has already made changes (the usual case for a rotation "revamp already in progress"), those changes almost always arrived as **strategies without stated objectives** — Step 4 before Steps 1–3. Don't discard them; make them explicit. For each existing change, fill:

| Change | Kern's step it lives in | Implied objective (Step 3 — make explicit) | Evaluation hook (Step 6 — attach) |
|---|---|---|---|

Then in Step 3, write a real SMART objective for each, and in Step 6, a real metric. This converts good instincts into a defensible, aligned curriculum and is typically the highest-value output of the analysis.

---

## 7. Word `.doc` export recipe (Drive-safe)

No pandoc/LibreOffice is needed. A `.doc` file whose contents are well-formed HTML opens natively in Word and Google Docs, with headings, bold, and tables rendered as real formatting (and no markdown hashmarks). Steps:

1. Compose the document as an HTML file (`<html>…<head><style>…</style></head><body>…</body></html>`). Use `<h1>/<h2>/<h3>`, `<table>`, `<ul>`, `<blockquote>`; inline the CSS in `<head>`. Give it a `.doc` extension.
2. **Write it to local scratch first** — not directly to the destination. Sandboxed file writes silently fail to reach Google Drive / network FUSE mounts (the write tool may even report success while nothing lands).
3. **Copy into the destination via shell**, disabling the sandbox for that copy if the destination is a Drive/FUSE mount:
   ```bash
   cp "<scratch>/<file>.doc" "<destination folder>/<file>.doc"
   ```
   Then `ls -la` the destination to confirm the byte size — don't trust a "created successfully" message alone.
4. On a Mac, Google Drive mounts live at `~/Library/CloudStorage/GoogleDrive-<account>/My Drive/…`; a `~/My Drive` path is usually the same mount. Both resolve to the same files.

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
