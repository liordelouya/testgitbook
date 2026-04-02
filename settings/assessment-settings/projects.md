# Projects

Projects connect assessors to control scopes, delegating assessment responsibilities within Lema. Configure them from **Settings → Projects**.

### Project List

All projects are listed in the left panel. Click any project to view and edit its configuration. Click **+ Add Project** to create a new one.

### Configuring a Project

Each project has two components:

**Members**

Add team members by name or email. Members assigned to a project are the assessors responsible for evaluating controls within that project's scopes. When a vendor is assessed under a project, its members are the ones notified and expected to act.

**Control Scopes**

Select which scopes belong to this project. The scopes assigned here determine which controls are evaluated when this project participates in an assessment.

A project can hold multiple scopes — for example, a Security project might include scopes for Critical vendors, High and above vendors, and sub-processors of PII, each activating based on the vendor's inherent risk profile.

### How Projects Work in Assessments

When starting a new assessment, you select one or more projects. Each project brings its assigned scopes into the assessment. If multiple projects participate — for example, Security and Legal — each contributes its own scopes and members, covering their respective controls within the same assessment.

{% hint style="info" %}
The controls evaluated in an assessment are determined entirely by the projects selected and the scopes attached to them. A control that isn't covered by any participating project's scope will not appear in the assessment.
{% endhint %}
