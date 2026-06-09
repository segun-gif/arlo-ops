# arlo-ops

**Coordination board for Arlo. Task queue only.**

This repo is **NOT the spec** — `CANON.md` lives in a private repo — and **NOT the seam log** — `INTEGRATION-STATE.md` lives in a private repo. Issues here are the **cross-agent task queue**. Agents execute **ONLY** issues labeled `approved`.

---

## The gate rule (hard rule)

> **Any agent may FILE a `proposed` issue. ONLY Segun moves `proposed` → `approved`. Agents execute ONLY `approved` issues. Filing ≠ authorization.**

---

## How the queue works

There is **no Projects board**. Status lives entirely in **status labels** on each issue. Filter the [Issues list](../../issues) by label to see each "column" of the queue:

- All proposed work → [`label:proposed`](../../issues?q=is%3Aissue+is%3Aopen+label%3Aproposed)
- Authorized to execute → [`label:approved`](../../issues?q=is%3Aissue+is%3Aopen+label%3Aapproved)
- Being worked → [`label:in-progress`](../../issues?q=is%3Aissue+is%3Aopen+label%3Ain-progress)
- Waiting on a dependency → [`label:blocked`](../../issues?q=is%3Aissue+is%3Aopen+label%3Ablocked)
- Completed → [`label:done`](../../issues?q=is%3Aissue+label%3Adone)

### Status labels (the gate)

| Label | Meaning |
|---|---|
| `proposed` | Filed, awaiting Segun's approval. **Not authorized to execute.** |
| `approved` | Segun has authorized execution. Agents may pick this up. |
| `in-progress` | An agent is actively working it. |
| `blocked` | Waiting on another open issue or an external dependency. |
| `done` | Completed; the `INTEGRATION-STATE.md` entry (private repo) is linked in the issue. |

### Function labels (routing)

`contracts` · `frontend` · `design` · `marketing` · `qa` · `security` · `docs` · `ops` · `community` · `bizdev`

---

## Assignee conventions

Some assignees are not GitHub users, so the assignee is recorded in the issue's **Assignee** field (text in the body), not GitHub's native assignee dropdown:

| Assignee | Who |
|---|---|
| `claude-code` | Claude Code — contracts / backend-on-chain. |
| `lovable` | Lovable — frontend / edge functions. |
| `advisory` | The advisory chat — review / adjudication. |
| `segun` | Founder. The **only** one who can move `proposed` → `approved`. |

---

## What this repo is NOT

- **Not** `CANON.md` (the signed spec) — private repo.
- **Not** `INTEGRATION-STATE.md` (the cross-agent seam record) — private repo.
- **Not** a place for contract code, deployed addresses, keys, or secrets.

Filing a task here is filing a request. It is authorized only when Segun labels it `approved`.
