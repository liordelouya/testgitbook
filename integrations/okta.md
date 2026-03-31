---
description: >-
  Pull user accounts, application assignments, group memberships, and admin
  roles from Okta into Lema.
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

# Okta

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Identity Provider</td><td></td></tr><tr><td>Data collected</td><td>Users, Applications, Groups, Admin roles</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Okta Super Administrator or Organization Administrator access</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Generate an API token

1. Sign in to your **Okta Admin Console**.
2. Go to **Security → API → Tokens** and click **Create Token**.
3. Give the token a name (e.g. `Lema Integration`) and set the allowed IP range to **Any IP**.
4. Copy the **token value** immediately.

{% hint style="warning" %}
The token value is shown only once. Copy it before closing this dialog.
{% endhint %}

5. Copy your **Okta domain** from the browser address bar (e.g. `https://yourorg.okta.com`).
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Okta**.
2. Enter your **Okta domain** and paste in your **API Token**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
