---
description: >-
  Pull cloud asset inventory, vulnerability findings, misconfigurations, and
  data security issues from Wiz into Lema.
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

# Wiz

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Cloud Security</td><td></td></tr><tr><td>Data collected</td><td>Cloud assets, Vulnerabilities, Configuration issues, Cloud accounts, Users, Data findings</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Wiz tenant admin access</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create a service account in Wiz

1. In your **Wiz console**, go to **Settings → Service Accounts**.
2. Click **Create Service Account**, give it a name (e.g. `Lema Integration`), and set the type to **Custom Integration**.
3. Assign the following API scopes:
   * `read:graph`
   * `read:inventory`
   * `read:configuration_rules`
   * `read:cloud_accounts`
   * `read:users`
   * `read:data_findings`
4. Click **Create** and copy the **Client ID** and **Client Secret**.

{% hint style="warning" %}
The Client Secret is shown only once. Copy it before closing this dialog.
{% endhint %}
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Wiz**.
2. Enter your **Tenant Data Center** — the Wiz regional API endpoint for your tenant (e.g. `api.us1.app.wiz.io`).
3. Enter the **Client ID** and **Client Secret** from Step 1.
4. Click **Add Integration**.
{% endstep %}
{% endstepper %}
