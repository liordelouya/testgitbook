---
description: Complete view of every vendor in your organization
---

# Third Parties

The Third Parties inventory is your complete view of every vendor your organization has a relationship with — sanctioned or not, assessed or not.

### The Inventory Table

Each row in the table represents a third party. At a glance you can see:

| Column                | What it shows                                                                     |
| --------------------- | --------------------------------------------------------------------------------- |
| **Third-party**       | Vendor name, description, and any affiliated relationship indicators              |
| **Lifecycle**         | Current status: In evaluation, Onboarded, Unsanctioned, Offboarded, or Archived   |
| **Assessment Score**  | Latest assessment result: Acceptable, Unacceptable, Concerning, or Never assessed |
| **Tags**              | Custom labels applied to the vendor                                               |
| **Data**              | Types of data the vendor accesses or processes                                    |
| **Findings**          | Open findings by severity (Critical, High, Medium)                                |
| **Sources**           | Integrations or intake sources this vendor was discovered through                 |
| **Re-assessment due** | Next scheduled assessment date, or cadence status                                 |

The lifecycle summary tiles at the top give you an instant count across each status — useful for a quick posture snapshot without filtering.

### Filtering and Search

Use the filter bar to slice your inventory by:

* **Inherent Risk** — filter by risk level
* **Lifecycle** — narrow to a specific status
* **Assessment Score** — surface vendors by their last assessment result
* **Tags** — filter by custom labels
* **Sources** — filter by where the vendor was discovered

Click **+ Add filter** for additional options including Data types, Findings, Usage, Business owner, Re-assessment due, and more.

{% hint style="info" %}
Unsanctioned vendors are highlighted in red. These are vendors detected in your environment that have not gone through a formal intake process — they require immediate attention.
{% endhint %}

### Exporting the Inventory

Click the export icon in the top right of the table to download the current view as a CSV. Filters applied to the table are reflected in the export.
