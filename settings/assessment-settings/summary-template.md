# Summary Template



Configure how Lema's AI generates executive summaries from **Settings → Summary**.

{% hint style="info" %}
Changes to the template apply to summaries generated after saving. To update a summary that was already generated, open it from the assessment, click **Edit**, then click **Regenerate**.
{% endhint %}

The template is made up of two layers: a set of general instructions that govern the AI's overall behavior, and individual section prompts that control what each part of the summary contains.

### General Instructions

The general instructions field sets the tone and constraints for the entire summary. The AI applies these rules across all sections before writing anything.

Use this field to define what the AI should and shouldn't do — for example, whether to include recommendations, how formal the language should be, or how to handle uncertainty in the data.

### Sections

Each section has a name and a prompt that tells the AI what to generate for that part of the summary. The default template includes sections such as:

* **Executive Summary** — a concise overview of the assessment outcome, vendor use case, and key findings
* **Business Context and Impact** — a narrative of the vendor's functional role based on their inherent risk profile, data types, and services

Click **+ Add section** to add a new section. Each section can be renamed and its prompt rewritten independently.

The AI generates each section in sequence, informed by both the section-level prompt and the general instructions above.

### Data used to preduce the summary

* Control outcomes and validation status
* Inherent risk profile
* Vendor profile
* Names of uploaded artifacts (not their content)
* Risks and findings
* Questionnaires
