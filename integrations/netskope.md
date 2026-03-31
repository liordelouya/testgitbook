---
description: >-
  Pull application event data from Netskope into Lema for visibility into cloud
  application usage across your organization.
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

# Netskope

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>SASE / Cloud Security</td><td></td></tr><tr><td>Data collected</td><td>Application Events</td><td></td></tr><tr><td>Setup time</td><td>~5 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Netskope Admin Console access</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create a REST API token

1. Log in to the **Netskope Admin Console**.
2. Navigate to **Settings → Tools → REST API v2**.
3. Click **New Token**, give it a name (e.g. `Lema Integration`), and assign the following endpoint scope:
   * `/api/v2/events/dataexport/events/application`
4. Click **Save** and copy the generated **API Token**.

{% hint style="warning" %}
The token value is shown only once. Copy it before closing this dialog.
{% endhint %}

5. Note your **Netskope domain** — find it in your browser address bar (e.g. `yourorg.goskope.com`).
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Netskope**.
2. Enter your **Netskope domain** and paste in your **API Token**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
