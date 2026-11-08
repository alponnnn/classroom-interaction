# Classroom Interaction System

> ITS 610204 / ITS 64604 — Principles of Software Engineering · Group Project · Semester September 2026
> Domain: **Smart Education** · Demonstration subject: **University Mathematics**

A classroom attendance and interaction system. The lecturer runs a quick check-in using a
time-limited code and gauges cohort understanding with in-class questions; each student's
attendance rate, correct-answer count and participation count are combined into a risk signal
so that the students who need attention become visible before the final examination.

---

## 1. Repository structure

The repository is organised by SDLC phase, as required by the assignment.

| Folder | Contents | Owner |
|---|---|---|
| `00_Planning/` | Team charter, WBS and timeline, risk register, contribution log, meeting minutes | A |
| `01_Requirements/` | FR and NFR registers, use case diagram, use case specifications, traceability matrix | B |
| `02_Design/` | Architecture, data model, sequence diagrams, wireframes, ADRs | C |
| `03_Test/` | Test plan, test cases, test results, defect log, UAT records | E |
| `04_Final/` | Prototype source, final report, presentation slides | A / D |

Every diagram is committed twice: the editable source (`.drawio`) **and** the exported `.png`.
The source file is the version-tracking evidence; the PNG is what goes into the report.

---

## 2. Running the prototype

The prototype is a static front-end and needs no installation.

1. Open `04_Final/prototype/index.html` in a browser.
2. To demonstrate the real-time interaction, open the same file in **two separate windows**:
   - left window → choose **Lecturer**
   - right window → choose **Student**
3. Start a check-in in the lecturer window; the student window updates immediately.

> **Prototype scope.** The prototype demonstrates real-time synchronisation across two browser
> windows on a single machine using the browser's same-origin messaging. Multi-device deployment
> over a network is out of scope for this prototype; the server-side design is specified in
> `02_Design/` but not implemented.

---

## 3. Team and roles

| ID | Member | Role |
|---|---|---|
| A | _to be filled_ | Project manager & integration lead |
| B | _to be filled_ | Requirements engineer |
| C | _to be filled_ | Solution architect & UI/UX designer |
| D | _to be filled_ | Prototype implementation |
| E | _to be filled_ | Testing & quality assurance |

---

## 4. Working agreements

See [CONTRIBUTING.md](CONTRIBUTING.md) for branch naming, commit format, the review rule and the
definition of done.
