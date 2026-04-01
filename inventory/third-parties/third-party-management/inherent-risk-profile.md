---
description: The risk a vendor poses to your organization
---

# Inherent Risk Profile

The Inherent Risk Profile tells you how much risk a vendor poses to your organization **before** any controls or mitigations are applied. It is driven by the **Inherent Risk Questionnaire (IRQ)** — a set of questions about the nature of your relationship with the vendor: what data they touch, how deeply they're integrated, what the operational impact of a failure would be, and more.

The result is an overall risk score — **Critical, High, Medium, or Low** — visualized as a radar chart across the risk dimensions defined in your IRQ.

{% hint style="info" %}
The IRQ questions and how they map to risk dimensions are fully customizable. See [IRQ Settings](../../../settings/third-party-settings/inherent-risk.md) for details. The radar chart dimensions reflect your configured IRQ structure.
{% endhint %}

{% hint style="warning" %}
Always verify the Inherent Risk Profile before starting an assessment. The IRQ determines which assessment scope applies to the vendor — an incomplete or inaccurate profile can result in the wrong controls being assessed.
{% endhint %}

### Filling the IRQ

Click **Edit** on the Inherent Risk Profile to open the IRQ.

{% stepper %}
{% step %}
### IRQ

Answer the questionnaire across each risk dimension. For each question, Lema surfaces **Smart Estimations** — AI-generated suggestions based on the vendor's profile, your integration data, and relationship context. Suggestions are shown inline with their source (AI projection or a connected integration such as Google Workspace).

You can:

* Select answers manually
* Click **Click to add** on individual suggestions to accept them one by one
* Click **Fill Suggested** to apply all AI suggestions at once
* Click **Reproject Org Company** to re-run the AI projection based on the latest vendor profile data

If the vendor was onboarded through the Request Portal, or an intage artifacts was uploaded, answers submitted by the business user during intake are automatically propagated here.
{% endstep %}

{% step %}
### Assign Inherent Risk

Lema computes a risk score from your IRQ answers. If business context requires it, a risk engineer can manually override the computed score. Overrides are tracked and attributed to the user who made them.

{% hint style="warning" %}
Overriding a risk profile disconnects it from all other logic and bases it solely on the risk defined by the risk engineer.
{% endhint %}
{% endstep %}
{% endstepper %}

### Risk Rollup from Engagements

When [engagements](third-party-engagements.md) are enabled for a vendor, each engagement carries its own Inherent Risk Profile. The vendor's overall inherent risk score is determined by the **most critical engagement** — risk rolls up from engagements to the parent vendor.

{% hint style="warning" %}
If a vendor has engagements enabled, the vendor-level IRQ reflects the aggregate of those engagements. Editing risk at the vendor level directly may be limited — manage risk at the engagement level instead.
{% endhint %}

### IRQ and Assessment Scope

The IRQ doesn't only produce a risk score — it can also determine which assessment scope applies to this vendor. See [Scopes](../../../settings/assessment-settings/scopes.md) for how risk levels map to assessment requirements.
