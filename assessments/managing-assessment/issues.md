---
description: All controls that require your attention in the assessment
---

# Issues

The Issues tab shows all unvalidated controls that require your attention in this assessment — controls where Lema found no evidence or identified a gap. The total count is displayed in the top right.

### Smart Evidence Request

At the top of the page is the **Smart Evidence Request** — a direct outreach to the vendor asking them to provide evidence or respond to specific control gaps.

Before sending:

* Click **+ Recipients** to select the vendor contacts who should receive the request
* Click **Pick a date** to set a response deadline
* Use the eye icon to preview exactly what the vendor will see

Click **Share** to publish the request. The vendor receives an email with a link to the Vendor Portal, where they can upload artifacts and respond to each control directly.

{% hint style="info" %}
As soon as the vendor uploads artifacts through the portal, Lema re-evaluates the relevant controls automatically and updates their validation status.
{% endhint %}

### Unvalidated Controls

The table lists every control that is not yet validated, sorted by weight. Columns:

| Column                | What it shows                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------- |
| **Control**           | Control name and category                                                                         |
| **Weight**            | How critical this control is to the overall score (1–5). Weight 5 controls are highlighted in red |
| **Findings**          | Any findings associated with this control                                                         |
| **Validation status** | Lema's current evaluation: No Evidence or Gap, with the time of last evaluation                   |
| **Review status**     | Manual review status set by your team                                                             |

### Control Detail

Click any control to open its detail panel:

* **Validation status** — Override Lema's result manually if needed. Once overridden, the status is locked and won't be updated automatically when new artifacts arrive
* **Control question** — The specific question being evaluated
* **Lema AI Insights** — A forensic explanation of what Lema found (or didn't find) in the vendor's artifacts, including the search terms used
* **Suggested Actions** — Concrete next steps recommended by Lema based on the current evidence gap
* **Activity** — A log of all actions and comments on this control, from both your team and the vendor

{% hint style="info" %}
Controls are re-evaluated automatically whenever new artifacts are uploaded, as long as the assessment is still open.
{% endhint %}
