---
description: >-
  Pull vendor records and spend data from Ramp into Lema to enrich third-party
  profiles with real purchasing activity.
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

# Ramp

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement</td><td></td></tr><tr><td>Data collected</td><td>Vendors, Spend data, Procurement requests</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Ramp admin access to create a developer application</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create a developer application in Ramp

1. Log in to your **Ramp account** and go to **Settings → Developers → Applications**.
2. Click **Create Application** and give it a name (e.g. `Lema Integration`).
3. Set the **Authorization type** to **Client Credentials**.
4. Copy the **Client ID** and **Client Secret**.

{% hint style="warning" %}
The Client Secret is shown only once. Copy it before closing this dialog.
{% endhint %}
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Ramp**.
2. Enter your **Client ID** and **Client Secret**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
