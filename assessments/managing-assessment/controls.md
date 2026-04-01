---
description: A full list of controls in scope for this assessment
---

# Controls

The Controls tab shows the full list of controls in scope for this assessment, their current validation status, and which scope they belong to. This is where you get a complete picture of what Lema has evaluated across all active scopes.

At the top of the page, each active scope appears as a tab — for example, _Business Continuity_ or _Privacy_. Click any tab to filter the list to controls from that scope only.

The number of scopes active in an assessment is determined by the vendor's Inherent Risk Profile. See Scopes for how activation rules work.

### Filtering and Grouping

* **Validation status** — filter by Validated, No Evidence, or Gap
* **Scope** — filter by scope group
* **Group by Scope** — toggle to organize controls under their scope headers
* **Search** — find a specific control by name

### Control Table

| Column                | What it shows                                     |
| --------------------- | ------------------------------------------------- |
| **Control**           | Control name and category                         |
| **Scope**             | Which scope this control belongs to               |
| **Findings**          | Any findings linked to this control               |
| **Validation status** | Lema's evaluation result and when it was last run |

### Control Drawer

Click any control to open its detail panel.

**Validation status buttons** — Set the status manually: **No Evidence**, **Gap**, or **Validated**. Once overridden, the status is locked and won't update automatically when new artifacts arrive. Click **Evaluate control** to re-run Lema's analysis on demand.

**Control question** — The specific question Lema is evaluating (e.g. _"Are access logs implemented in the company's environments?"_).

**Lema AI Insights** — Lema's verdict and reasoning, broken into two parts:

* **Summary** — A plain-language conclusion (Yes / No / Unclear) with a concise explanation of what was found
* **Details** — The full forensic explanation, including the exact search terms used and what the documents contained

**Evidence** — Every artifact that contributed to the evaluation is listed with:

* The document name and page number where evidence was found
* The exact quotes Lema extracted from the document
* A **Copy quotes** button to quickly copy the evidence for use in reports or follow-ups

**Activity** — A log of all actions and comments on this control from your team and the vendor.

{% hint style="info" %}
Controls are re-evaluated automatically whenever new artifacts are uploaded to this assessment, as long as it remains open.
{% endhint %}
