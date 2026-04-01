---
description: Approve or reject the vendor for the current assessment cycle
---

# Concluding an Assessment

The Conclusion tab is where a risk engineer reviews the full picture and renders a final decision — approve or reject the vendor for the current assessment cycle.

### Assessment Summary

At the top of the tab, Lema surfaces a summary of control outcomes across all scopes:

* **Validated** — controls confirmed with sufficient evidence
* **Gap** — controls evaluated as non-compliant or insufficient
* **No Evidence** — controls not evaluated due to missing documentation

The assessment score is recalculated based on these outcomes. The score label (e.g., **Concerning**, **Moderate**, **Low Risk**) reflects the weighted result across all scopes and is the same score visible in the assessment overview.

Use this summary as your final sanity check before writing the conclusion and issuing a decision.

### Writing the Conclusion

The conclusion is a free-text field for documenting your reasoning, risk narrative, and any conditions attached to the decision.

This field is **collaborative** — multiple team members can write and edit simultaneously, and changes sync in real time. Use it to capture:

* A summary of key findings and gaps
* Context that isn't captured in control outcomes
* Any mitigating factors or compensating controls the vendor provided
* Conditions the vendor must meet before the next review

There's no required format. Write as much or as little as your process demands.

### Issuing a Decision

Once you're ready, click **Approve** or **Reject**.

{% tabs %}
{% tab title="Approve" %}
The assessment is marked as approved. The vendor's assessment status updates in the inventory and the assessment is closed.
{% endtab %}

{% tab title="Reject" %}
The assessment is marked as rejected. You can include a note explaining the rejection — this is visible in the audit trail and on the vendor's assessment history.
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
Decisions are permanent. Once an assessment is approved or rejected, it cannot be reopened. If a new review is needed, start a new assessment.
{% endhint %}

### Audit Trail

The conclusion text, decision, and timestamp are recorded in the audit trail and permanently linked to the assessment record. You can review past conclusions from the **Past Assessments** table on the vendor's profile.
