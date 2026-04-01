---
description: >-
  The actual access rights the vendor has been granted to your organization's
  systems
---

# Permissions

The Permissions tab shows the actual access rights and OAuth scopes this vendor has been granted to your organization's systems — pulled directly from your connected identity and productivity integrations.

This is real, live data. Not what a vendor claims in a questionnaire — what they can actually do in your environment right now.

### What You're Seeing

Each row is an individual permission granted to this vendor, showing:

* **Permission** — the specific OAuth scope or API permission
* **Description** — what that permission allows the vendor to do
* **Category** — how Lema classifies the permission by risk type (e.g., Employee Data Access, Employee Data Modification)
* **Source** — the integration it was detected through (e.g., Google Workspace, Okta)

Permissions are grouped by **Category** by default, making it easy to spot high-risk access patterns at a glance.

### Why It Matters

Most TPRM programs rely on vendors self-reporting their access. Lema surfaces permissions automatically from your connected systems — giving you an evidence-based view of blast radius before an incident happens.

Use this tab to:

* Identify vendors with access beyond what's expected for their role
* Detect scope creep — permissions that have accumulated over time
* Validate that offboarded vendors no longer have active access

{% hint style="info" %}
Permissions data is sourced from your active integrations. Connect Google Workspace, Okta, Microsoft Entra ID and others to populate this tab.
{% endhint %}
