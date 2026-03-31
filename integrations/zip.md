---
description: >-
  Pull vendor records and procurement requests from Zip into Lema to streamline
  third-party intake and risk assessment.
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

# Zip

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement</td><td></td></tr><tr><td>Data collected</td><td>Vendors, Procurement Requests</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Zip admin access</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create a restricted API key

1. Log in to your **Zip admin account** and navigate to **Settings → API Keys**.
2. Click **Create New Key** and select **Restricted**.
3. Grant **Read Only** access for the following resource types:
   * Requests
   * Vendors
   * Documents
   * Approvals
4. Copy the **API Key** value.

{% hint style="info" %}
Using a restricted, read-only key follows the principle of least privilege — Lema only needs to read data, not write it.
{% endhint %}
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Zip**.
2. Paste in your **API Key**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
