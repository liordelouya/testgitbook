---
description: >-
  Pull supplier records and vendor risk data from Coupa into Lema using OAuth2
  client credentials.
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

# Coupa

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement</td><td></td></tr><tr><td>Data collected</td><td>Suppliers / Vendors</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Coupa admin access to create an OAuth2 client</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create an OAuth2 client in Coupa

1. Log in to your **Coupa instance** and go to **Setup → Integration → OAuth2/OpenID Connect Clients**.
2. Click **Create** and fill in the following:
   * **Grant Type:** Client Credentials
   * **Name:** e.g. `Lema Integration`
3. Assign the following required scopes:
   * `core.suppliers.read`
   * `core.supplier_information.read`
   * `core.supplier_information.risk_and_compliance.read`
   * `core.common.read`
4. Save the client and copy the **Identifier** (client ID) and **Secret**.
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Coupa**.
2. Enter your **Resource URL** — your Coupa instance hostname, without `https://`.

{% hint style="info" %}
For example, if your Coupa URL is `https://yourorg.coupahost.com`, enter `yourorg.coupahost.com`.
{% endhint %}

3. Enter the **Identifier** and **Secret** from Step 1.
4. Click **Add Integration**.
{% endstep %}
{% endstepper %}
