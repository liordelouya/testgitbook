---
description: Manually add a vendor to your inventory
---

# Adding a Third Party

To manually add a vendor to your inventory, click **+ Add Third-Party** in the top right of the Inventory page.

{% stepper %}
{% step %}
### Profile

Search for the vendor by name. Lema will attempt to auto-match it to a known company and pre-fill basic profile details (category, size, website).

Set the **Lifecycle** to reflect where this vendor currently stands:

* **In evaluation** — vendor is being considered
* **Onboarded** — vendor is active and approved
* **Archived** — vendor is no longer active but kept for records
* **Offboarded** — vendor relationship has been terminated

{% hint style="warning" %}
**A note on domain**

Lema uses the vendor's domain to automatically enrich the vendor profile — pulling in findings, data exposure signals, and other intelligence from connected sources. Without a domain, this enrichment won't happen.
{% endhint %}

{% hint style="info" %}
If you're adding a third-party without a domain, consider whether it should be created as an [Affiliated Third-Party or Engagement](third-party-affiliates.md). This keeps your inventory clean and maintains the relationship to the parent vendor. See Third-Party Affiliates for more.
{% endhint %}
{% endstep %}

{% step %}
### Assessment

Choose whether this vendor requires an assessment:

* **Yes, assessment is required** — select the assessment project(s) to open. They will be created in _Ready to start_ status.
* **No, it is already assessed** — skip assessment creation and add the vendor to inventory as-is.
{% endstep %}

{% step %}
### Artifact Upload

Upload any existing documents for this vendor — SOC 2 reports, penetration test results, security questionnaires, or any other relevant artifacts. This step is optional and can be done later.

Click **Finish** to create the vendor record.
{% endstep %}
{% endstepper %}
