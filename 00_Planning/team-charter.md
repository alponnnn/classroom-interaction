# Team Charter

**Project:** Classroom Interaction System
**Module:** ITS 610204 — Principles of Software Engineering
**Semester:** September 2026
**Domain:** Smart Education
**Version:** v1.0 — adopted at kickoff

---

## 1. Problem

1. **Roll call consumes class time.** A paper or verbal roll call takes five to ten minutes and in
   practice only covers a sample of the class.
2. **Attendance data cannot be trusted.** With a fixed QR code or a signed sheet, proxy attendance
   is almost impossible to detect, which makes the resulting data useless for any later analysis.
3. **Classroom feedback arrives too late.** After teaching a concept the lecturer has no way to know
   how many students followed it, and finds out at the examination — when it is too late to reteach.

The common thread: the problem is not that attendance is not recorded. It is that the record is
neither trustworthy nor used to improve teaching.

## 2. Proposed system

A single-classroom attendance and interaction system. The lecturer runs a check-in with a
time-limited code and gauges cohort understanding with in-class questions. Each student's
attendance rate, correct-answer count and participation count are combined into a risk signal,
so that students needing attention surface before the final examination.

## 3. Actors

| Actor | Description |
|---|---|
| Student | Attends the class, checks in, answers in-class questions, asks questions |
| Lecturer | Runs the check-in, poses in-class questions, monitors participation and risk |

The programme administrator is identified as a stakeholder but **no use case serves this role
within the defined scope**, so it is not an actor on the use case diagram.

## 4. Intelligent capabilities

| Capability | Mechanism | Problem addressed |
|---|---|---|
| Time-limited check-in code | Code refreshes every 30 seconds and expires | Codes photographed and forwarded to absent classmates |
| Live comprehension check | In-class answers aggregated in real time | Lecturer cannot tell whether a concept landed |
| Risk identification | Attendance rate + correct-answer count + participation count | A single absence says nothing; only the trend does |

**Stated limitation:** a refreshable code reduces proxy attendance but cannot prevent it — a code
can still be forwarded within its window. The system therefore reports risk rather than proving
identity.

## 5. Scope

**In scope.** One class group; two roles; six screens; real-time synchronisation across two
browser windows on one machine; pre-loaded synthetic data; two to three in-class questions.

**Out of scope, deliberately.** Face recognition or any biometric identification; Bluetooth, NFC or
Wi-Fi presence detection; synchronisation across devices over a network; integration with the
university academic system; real student data; production authentication and push notification;
timetable and room management; late-arrival statistics.

**Data policy.** All names, attendance records and answers used in the prototype are synthetic.
No real student record is used at any point.

## 6. Roles

| ID | Member | Role | Owns |
|---|---|---|---|
| A | | Project manager & integration lead | Plan, repository, traceability matrix, report consolidation, slides |
| B | | Requirements engineer | FR/NFR registers, use case content and descriptions |
| C | | Solution architect & UI/UX designer | All UML diagrams, data model, wireframes |
| D | | Prototype implementation | Check-in code, real-time sync, risk scoring, student screens |
| E | | Testing & quality assurance | Test plan, test cases, execution, defect log, UAT |

## 7. Working agreements

- **Cadence.** Weekly sync, sixty minutes, Monday evening. Asynchronous daily check-in in the group
  channel. A short retrospective at the end of each sprint, committing to change one practice.
- **Single source of truth.** If an artefact is not in the repository, it does not exist. Chat
  messages and personal drives are not deliverables.
- **Early warning.** Anyone who cannot meet an agreed date says so at least 48 hours in advance and
  proposes a re-plan. Silent slippage is treated as a process problem, not a personal one.
- **Definition of done.** Committed to the correct SDLC folder, reviewed by one other member, and
  referenced from the traceability matrix.

## 8. Tools

| Purpose | Tool | Reason |
|---|---|---|
| Artefact store, version tracking, task board | GitHub (repository + Projects) | The assignment requires artefact management and version tracking to be unified; hosting both in one place avoids a gap between the task list and the artefacts |
| UML modelling | draw.io | `.drawio` is a text format, so diagram revisions can be diffed in Git; Visio's binary format cannot be compared |
| UI wireframes | Figma | Shared links and version history allow the low-fidelity to high-fidelity progression to be shown during the presentation |
| Test registers | Excel | Test cases, results and defect log map one-to-one onto the three testing artefacts the rubric asks for |
