---
description: A shareable executive summary of every assessment
---

# Assessment Summary

Once an assessment is concluded, Lema's AI automatically generates a shareable executive summary. This summary is designed for security leadership, legal, procurement, and business owners. It translates control-level outcomes into business-ready language: high-level risk posture, key findings, and their implications.

**Data sources the AI uses:**

* Control outcomes and validation status
* Inherent risk profile
* Vendor profile
* Names of uploaded artifacts (not their content)
* Risks and findings
* Questionnaires

The generated summary is fully editable. Click into any section to rewrite, remove, or add context before sharing.

### Controlling the AI Output

Admins control how the AI generates executive summaries by managing the prompt template in **Settings → Assessment Summary Templates**.

You can write one general prompt that governs the full summary, or define per-section prompts — for example, separate instructions for the Risk Overview, Key Gaps, and Recommendations sections. This lets you control tone, structure, and level of detail consistently across every assessment.

From the template settings you can:

* Edit the default prompt and structure
* Recreate the template entirely from scratch
* Set global or per-section AI instructions

Changes apply to all summaries generated after the template is saved. To regenerate an existing summary using an updated template, open the executive summary, click **Edit**, then click **Regenerate**.

{% hint style="info" %}
You're not locked into Lema's default language. The prompt template gives admins full control over how the AI writes — globally and consistently across your team.
{% endhint %}

Learn more about [Assessment Summary Template](../settings/assessment-settings/summary-template.md)
