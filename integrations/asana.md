---
description: >-
  Pull vendor and procurement request data from Asana tasks into Lema to
  automate third-party intake from your existing workflows.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Asana

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement</td><td></td></tr><tr><td>Data collected</td><td>Third-parties (vendor details from Asana tasks)</td><td></td></tr><tr><td>Setup time</td><td>~5 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>An Asana account with a project configured for vendor intake</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Generate a Personal Access Token

1. Log in to Asana and go to **My Profile → My Apps → Create New Personal Access Token**.
2. Give the token a name (e.g. `Lema Integration`) and copy the generated value.

{% hint style="warning" %}
The token value is shown only once. Copy it before closing this dialog.
{% endhint %}
{% endstep %}

{% step %}
#### Find your Project ID

Open the Asana project you want to connect and copy the **Project ID** from the URL.

{% hint style="info" %}
The Project ID is the numeric string in the URL path: `https://app.asana.com/0/`**`123456789`**`/...`
{% endhint %}
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Asana**.
2. Enter your **Personal Access Token** and **Project ID**.
3. Click **Connect**.
{% endstep %}

{% step %}
#### Map custom fields

After connecting, map your Asana task fields to Lema fields:

| Lema field | Asana field to map |
|---|---|
| Vendor name | The field containing the vendor or supplier name |
| Website | The field containing the vendor's website URL |
| Request name | The field to use as the procurement request name in Lema |
{% endstep %}

{% step %}
#### Configure Engagement Mode (optional)

Turn on **Engagement Mode** if you want Lema to write status updates back to Asana as assessments progress. When enabled, Lema will update the corresponding Asana task status when key assessment milestones are reached.
{% endstep %}
{% endstepper %}
