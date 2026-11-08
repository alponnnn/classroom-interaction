# Contributing

Rules that keep the artefact history readable. They are deliberately few.

## Branches

`main` is protected — nobody pushes to it directly.

```
main                        stable, always presentable
feat/<name>-<topic>         e.g. feat/wei-usecase-diagram
fix/<name>-<topic>          e.g. fix/lin-grading-null
```

## Merge

Open a pull request against `main` and have **at least one other member review it** before
merging. The reviewer is the owner of the affected area, or the project manager by default.

## Commit messages

```
<type>(<area>): <what changed>
```

| Type | Use for |
|---|---|
| `docs` | report chapters, minutes, registers, diagrams |
| `feat` | new prototype behaviour |
| `fix` | defect correction |
| `test` | test cases, results, defect log |
| `chore` | repository housekeeping |

Examples:

```
docs(req): add FR-01 to FR-12
docs(design): architecture diagram v1 with ADR-001
test(cases): add TC-01 to TC-22 for check-in flow
fix(checkin): reject codes older than 30 seconds
```

Avoid `update`, `修改`, `1`, `final final`. They tell the reader nothing and they are the
single most common way to lose marks on tool usage.

## Definition of done

An artefact counts as complete only when **all three** are true:

1. it is committed to its correct SDLC folder;
2. it has been reviewed by one other member;
3. **it is referenced from the traceability matrix.**

Condition 3 is what stops artefacts from being forgotten and keeps the traceability matrix
alive throughout the project rather than reconstructed at the end.

## Folder rules

- Put the file in the folder named after the SDLC phase it belongs to — not in a personal folder.
- Commit diagrams as both `.drawio` and `.png`.
- Name files predictably: `use-case-diagram.drawio`, `FR_Register.xlsx`, `test-results.xlsx`.
- Never commit: personal notes, screenshots of chats, `.DS_Store`, temporary exports.

## Before you start work each day

```
git pull
```
