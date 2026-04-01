---
description: >-
  The sub-processor or service provider that your third parties rely on to
  deliver their services
---

# Fourth Parties

A fourth party is a vendor of your vendor — a sub-processor or service provider that your third parties rely on to deliver their services to you. You don't contract with them directly, but they are part of your risk surface.

When a major provider like a cloud platform or AI infrastructure company has an outage or breach, the first question is: _"Which of our vendors are affected?"_ Fourth-party visibility lets you answer that in seconds.

Lema automatically discovers fourth parties by scanning public artifacts — SOC 2 reports, Data Processing Agreements, privacy policies, and trust centers — across your vendor inventory. The map updates continuously as new artifacts are collected.

{% hint style="info" %}
Fourth-party discovery is fully automated. You cannot manually add or remove fourth parties — they are derived from evidence Lema finds in vendor artifacts.
{% endhint %}

### Fourth-Party Inventory

Navigate to **Fourth-parties** to see a global table of all fourth parties detected across your vendor portfolio.

The table is sorted by number of dependent third parties — the vendors in your inventory that rely on each fourth party — making concentration risk immediately visible.

| Column               | What it shows                                         |
| -------------------- | ----------------------------------------------------- |
| **Fourth-party**     | Name and description of the sub-processor             |
| **Third-parties**    | Number of your vendors that rely on this fourth party |
| **Industry**         | Fourth party's industry classification                |
| **Primary location** | Countries where the fourth party operates             |

Filter by **Industry** or **Primary location** to identify offshore exposure or sector-specific dependencies. Use the search bar to look up a specific provider — for example, when news breaks about a company and you need to know your exposure immediately.

### Fourth-Party Drawer

Click any fourth party to open its drawer. It shows a **Dependent third-parties** table — every vendor in your inventory that uses this fourth party as a sub-processor.

For each dependent vendor you can see:

* **Inherent risk and lifecycle** — the risk level and current status of that vendor
* **Purpose** — what the fourth party is used for within that vendor's service
* **Data location** — where the fourth party processes or stores data on that vendor's behalf
* **Evidence** — a link to the source document (e.g., the vendor's sub-processor list) and the effective date of the relationship

### Fourth Parties on the Vendor Profile

Every vendor profile includes a **Fourth-parties** tab showing the sub-processors that specific vendor relies on. This gives you a focused view for a single relationship — useful during an assessment or when reviewing a specific vendor's supply chain.

### Why It Matters

{% columns %}
{% column %}
**Incident response** Search for a breached or unavailable provider and instantly see which of your vendors are exposed — no manual cross-referencing.
{% endcolumn %}

{% column %}
**Concentration risk** Identify hidden single points of failure where many vendors depend on the same underlying fourth party.
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column %}
**Regulatory compliance** Maintain documented visibility into your sub-processor ecosystem to meet requirements under DORA, FDIC guidance, and similar frameworks.
{% endcolumn %}

{% column %}
**Portfolio diversification** Spot lesser-known fourth parties shared across many vendors and factor supply-chain diversity into your vendor selection.
{% endcolumn %}
{% endcolumns %}
