---
description: A distinct scope of work or relationship within a single vendor
---

# Engagements

An engagement represents a distinct scope of work or relationship within a single vendor — a new product, a feature addition, a service expansion, a contract renewal, or any change that meaningfully affects how you use that vendor.

Every meaningful touchpoint with a vendor is an engagement. For example, with Atlassian:

* Starting with Jira → first engagement
* Adding Confluence → new engagement
* Enabling Atlassian AI features → new engagement
* Renewing the contract with additional sites → new engagement

Each engagement has its own **Inherent Risk Profile**. As engagements are added, their risk rolls up to the vendor — the vendor's overall risk is determined by the highest risk of its engagements. Once engagements are enabled, the vendor-level risk profile cannot be edited directly.

{% hint style="info" %}
Engagements share the vendor's findings, controls, and artifacts. This is the core distinction from Affiliated Third Parties — which have their own independent set of each. If a relationship needs separate artifacts or controls, it should be an affiliated third-party, not an engagement.
{% endhint %}

### Enabling Engagements

Engagements are not enabled by default. To turn them on, click **Enable engagements** on the vendor's Inherent Risk Profile section.

When you enable engagements:

* You are prompted to name and describe the first engagement — this becomes the **Default** engagement
* The vendor's existing Inherent Risk Profile is moved under this first engagement
* From this point, all risk is managed at the engagement level

### Adding Engagements

Once enabled, click **+ Add engagement** on the vendor profile to create a new engagement. Each engagement has:

* **Name and description** — what this engagement covers
* **Inherent Risk Profile** — its own IRQ, filled and validated independently
* **Tags, Business Owner, Points of Contact, and Custom Fields** — scoped to this engagement

Click **Open** on any engagement to open its full detail drawer.

{% hint style="warning" %}
Disabling engagements will **permanently delete** all engagements and their data. This cannot be undone.
{% endhint %}

### How Engagements Drive Risk and Assessment Scope

Each engagement's IRQ contributes to the vendor's overall risk profile. When an engagement introduces a new data type or increases risk on any dimension, this propagates to the vendor level and can trigger a new assessment scope.

This means assessments are scoped at the vendor level but driven by what the engagements collectively declare. Validating each engagement's Inherent Risk Profile before starting an assessment ensures the right controls are in scope.

### Viewing Engagements

All engagements across your inventory are visible from the **Engagements** Inventory page. This gives you a cross-vendor view of every active engagement — useful for spotting scope creep or prioritizing reviews.

Affiliated third-parties can also have their own engagements, following the same model.
