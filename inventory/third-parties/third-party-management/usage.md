---
description: >-
  Who in your organization is actively using this vendor and how usage is
  distributed
---

# Usage

The Usage tab shows who in your organization is actively using this vendor and how usage is distributed — pulled directly from your connected integrations.

Like Permissions, this is live data from your environment, not vendor self-reporting.

### Summary

At the top of the tab, three panels give you an instant snapshot:

* **By Line of Business** — how usage is distributed across your organization's departments and teams
* **Total Users** — the total number of employees with active access to this vendor
* **Datatypes** — the categories of data being accessed or processed through this vendor

Use the **All Solutions** dropdown to filter by a specific connected integration if the vendor has multiple.

{% hint style="info" %}
The Datatypes panel reflects what Lema has detected through your connected integrations. To get a more complete picture, connect additional integrations from Settings.
{% endhint %}

### Users

The Users table lists every employee in your organization who has authorized or accessed this vendor, showing:

* **User Name and Email** — the individual employee
* **Last Authorization** — the most recent date they authenticated or accessed the vendor
* **Source** — the integration this was detected through

Use this to identify unexpected users, flag access from employees who have left, or understand the blast radius if this vendor were compromised.

{% hint style="info" %}
Usage data is sourced from your active integrations. Connect Google Workspace, Okta, Microsoft Entra ID and others to populate this tab.
{% endhint %}
