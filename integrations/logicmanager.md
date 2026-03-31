---
description: >-
  Pull third-party relationship records and supporting documents from
  LogicManager into Lema.
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

# LogicManager

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement / GRC</td><td></td></tr><tr><td>Data collected</td><td>Third-Parties (Relationships), Documents</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>LogicManager admin access</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Gather your API credentials

Follow LogicManager's internal API documentation to retrieve the following four values:

* **API Key** — your account's primary API key
* **Global API Key** — the organization-wide key required for cross-program access
* **Username** — your LogicManager account email
* **Domain** — your LogicManager instance hostname

{% hint style="warning" %}
Use the format `XXXX.logicmanager.com`, **not** `XXXX.my.logicmanager.com`. The wrong domain format will cause the connection to fail.
{% endhint %}
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → LogicManager**.
2. Enter your **API Key**, **Username**, **Domain**, and **Global API Key**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
