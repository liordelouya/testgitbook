---
description: Adversarial signals automatically detected from public data sources
---

# Findings

Findings are adversarial signals automatically detected from public data sources. Lema continuously monitors your vendor inventory and surfaces findings as they emerge — no manual searches required.

Each finding represents a real-world event that may indicate increased risk exposure: an outage, a disclosed breach, a lawsuit, or a structural change at the vendor. Findings flow directly to the relevant third-party profiles and can be used as evidence when validating controls in an assessment.

### Finding Types

| Type                                  | What it captures                                                |
| ------------------------------------- | --------------------------------------------------------------- |
| **Service Outage Disclosure**         | Reported disruptions to the vendor's services or infrastructure |
| **Security Vulnerability Disclosure** | Published CVEs or disclosed security weaknesses                 |
| **Data Breach**                       | Confirmed or reported exposure of customer or internal data     |
| **Material Litigation Filing**        | Significant legal actions filed against the vendor              |
| **Workforce Reduction**               | Layoffs or major organizational restructuring events            |
| **Bankruptcy Filing**                 | Insolvency proceedings or financial distress disclosures        |

### The Findings Table

The Findings table shows all detected findings across your entire vendor inventory in one view. Use the filters to focus on what matters — for example, High severity findings against Critical or High inherent risk vendors, or open findings within a specific scope.

### Reviewing a Finding

Click any row to open the finding drawer.

**Finding Overview tab**

* **Control** — the control this finding is linked to (e.g. Outage History, Vulnerability Management)
* **Description** — what was detected and what it means in context
* **What is the Risk?** — the potential business and security impact if the issue is unresolved
* **Suggested Actions** — AI-generated remediation steps you can copy and act on
* **Evidence** — the raw signal that triggered the finding: incident title, duration, impact level, affected components, and a direct link to the source

**Activity tab**

A log of status changes, notes, and any actions taken on the finding.

### Managing a Finding

From the drawer header you can:

* **Severity** — adjust the severity level if the default doesn't reflect your organization's exposure
* **Work Status** — update the status as you triage (Open, In Progress, Resolved)
* **Hide finding** — remove it from the active view without marking it as false positive
* **False Positive** — flag it as a false positive to exclude it from risk calculations
* **Export** — export the finding details for reporting or escalation

### Using Findings as Control Evidence

Findings can be applied directly as evidence when evaluating controls in an assessment. If a vendor has an open Service Outage finding, for example, it can be cited when assessing their Business Continuity or Incident Response controls — without needing to upload a separate document.

{% hint style="info" %}
Findings are sourced exclusively from public data. Lema does not scan vendor systems or access non-public information to generate findings.
{% endhint %}
