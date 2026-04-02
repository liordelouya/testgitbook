---
description: Apply controls based on a vendor's inherent risk level and IRQ responses
---

# Scopes

Scopes define which controls apply in an assessment and when. Rather than evaluating the same controls for every vendor, Lema activates controls based on a vendor's inherent risk level and IRQ responses — so assessments are scoped to actual exposure.

The result is less noise for low-risk vendors, sharper focus on high-risk ones, and a faster assessment process for everyone.

### How Scopes Work

Each scope defines:

* Which controls may be evaluated
* When those controls activate, based on vendor risk attributes

Scopes are attached to **projects**. When an assessment starts, Lema evaluates the scope rules for that project and includes only the controls from applicable scopes. Multiple scopes can be active within a single assessment.

{% hint style="info" %}
Each control can belong to only one scope at a time. Assigning a control to a new scope automatically removes it from its previous one. Plan your scope structure before assigning controls.
{% endhint %}

### Managing Scopes

Navigate to **Settings → Scopes** to create, edit, or delete scopes.

Each scope in the list displays:

* Name and description
* Assigned project
* Number of controls
* Number of activation rules

### Creating a Scope

{% stepper %}
{% step %}
#### Define Scope Details

Provide a **name**, **description**, and select a **project**.

The name should clearly reflect the scenario the scope covers — for example, "High Risk – Data Processing." The description should explain when and why it applies.

Scopes must be assigned to a project. Once configured, a scope is only evaluated within its assigned project.
{% endstep %}

{% step %}
#### Add Controls

Select the controls that should run when this scope is triggered.

Disabled controls remain visible in the scope but will not run during assessments. A scope must include at least one control before it can be saved.
{% endstep %}

{% step %}
#### Define Activation Rules

Activation rules determine when the scope becomes active for a given vendor. Scopes can be triggered by:

* **Inherent Risk (IR) level** — e.g., activate for Critical and High vendors only
* **IRQ responses** — e.g., activate when the vendor processes customer health information

You can combine both condition types to create precise evaluation logic.
{% endstep %}
{% endstepper %}

### Behavior in Active and Past Assessments

**Past assessments** are immutable. Changes to a scope's controls or activation rules do not add or remove controls from completed assessments.

**Active assessments** update dynamically. If a scope or inherent risk configuration changes while an assessment is in progress, controls may be added or removed immediately — keeping the assessment aligned to the current scope configuration.
