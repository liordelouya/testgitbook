---
description: Structured questionnaire to calculate a vendor's inherent risk level
---

# Inherent Risk

The IRQ is the structured questionnaire Lema uses to calculate a vendor's inherent risk level — editing it changes how risk is projected across your entire inventory.

### Structure

The IRQ is organized into **sections** and **questions**. The right-hand panel gives you a navigable outline of the full questionnaire. Sections group related questions together — for example, Data, Spend, Operational Impact, Attack Surface, and Service Delivery.

Use the drag handles to reorder sections and questions. Click the three-dot menu on any section or question for additional options.

### Editing a Question

Click any question in the right panel to open it in the editor.

**Question types**

Each question can be set to one of three types:

* **Text** — open-ended free text response
* **Single select** — one answer from a predefined list
* **Multi select** — one or more answers from a predefined list

**Answer options and risk levels**

For select-type questions, each answer option is assigned a risk level — Critical, High, Medium, or Low. When a vendor's IRQ is filled in, Lema uses these answer-level risk assignments to calculate the overall inherent risk score.

For example, if a vendor selects "Customer Health Information" as a data type, that answer carries a Critical risk weight. The combination of answers across all sections determines the projected inherent risk level.

**Optional description**

Add a description to any question to give context to the person filling in the IRQ.

### Adding Sections and Questions

Use the three-dot menu on any section to add a new question within it, or add a new section from the panel. Newly added questions follow the same structure: question type, answer options, and per-answer risk level.

### Resetting to Default

Click **Reset to default** to restore the Lema-recommended IRQ template. This will overwrite any customizations you have made.

{% hint style="warning" %}
Changes to the IRQ affect how inherent risk is projected for all vendors. Existing vendors whose IRQ has already been completed will not be automatically re-evaluated — a re-projection or manual review may be required.
{% endhint %}
