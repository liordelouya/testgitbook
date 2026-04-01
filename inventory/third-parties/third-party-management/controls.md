---
description: All control evaluated for a given vendor
---

# Controls

The Controls tab shows every control evaluated for this vendor, along with its current validation status. The status displayed reflects the outcome from the **most recent assessment**.

### Control Statuses

Controls are grouped into three statuses, visible as quick-filter tabs at the top:

* **Validated** — Lema found evidence in the vendor's artifacts confirming the control is in place
* **No Evidence** — Lema could not find sufficient evidence to confirm or deny the control
* **Gap** — The control is explicitly missing or the vendor failed to demonstrate it

### Filtering and Grouping

Filter controls by **Scope** or use **+ Add filter** to narrow by other attributes. Toggle **Group by Scope** to organize the list by assessment scope — useful when a vendor has multiple scopes active.

### Control Evaluation Data

Click any control to open its detail drawer. It shows:

* **Scope** — which assessment scope this control belongs to
* **Control question** — what Lema is evaluating
* **Lema AI Insights** — a forensic summary of what was found (or not found) in the vendor's artifacts, including the specific search terms used and what the documents contained
* **Suggested Actions** — concrete next steps recommended by Lema based on the current evidence gap
* **Validation Status** — manually set or confirm the status: **Validated**, **No Evidence**, or **Gap**

{% hint style="info" %}
Lema evaluates controls automatically when artifacts are uploaded and assessment is ongoing. The timestamp shown on each control reflects when it was last evaluated.
{% endhint %}

For details on how controls are defined and configured, see [Controls Settings](../../../settings/assessment-settings/controls.md).
