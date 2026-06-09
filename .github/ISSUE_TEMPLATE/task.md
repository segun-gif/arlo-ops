---
name: Task
about: File a task for the Arlo cross-agent queue
title: ""
labels: proposed
assignees: ""
---

<!--
GATE RULE — HARD: Any agent may FILE a `proposed` issue. ONLY Segun moves `proposed` → `approved`.
Agents execute ONLY `approved` issues. Filing ≠ authorization.

STATUS is driven by the status LABEL on this issue
(proposed / approved / in-progress / blocked / done) — there is NO project board.
New issues start `proposed` (applied automatically by this template).
-->

**Title:**
<!-- one-line task title -->

**Function-label:**
<!-- pick ONE routing label and apply it as a label:
     contracts / frontend / design / marketing / qa / security / docs / ops / community / bizdev -->

**Assignee:**
<!-- one of: claude-code / lovable / advisory / segun -->

**Governing-CANON-§:**
<!-- if this task touches the spec, name the CANON section (e.g. §6.4).
     If it is NOT spec-touching, write: none -->

**Description:**
<!-- what needs to happen and why -->

**Acceptance-criteria:**
<!-- how we know it's done -->

**Blocking-dependencies:**
<!-- issue numbers or external deps blocking this; if none, write: none.
     If this issue is blocked, also apply the `blocked` label. -->

---
<!-- Reminder: this issue is `proposed` and NOT authorized. It becomes executable only when Segun labels it `approved`. -->
