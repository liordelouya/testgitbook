---
description: >-
  Connect OneTrust to sync vendor intake data into Lema — or enable
  bi-directional sync to push risk findings back to OneTrust.
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

# OneTrust

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement / GRC</td><td></td></tr><tr><td>Data collected</td><td>Third-party intake data (inbound) · Control gaps and Artifacts (outbound, bi-directional only)</td><td></td></tr><tr><td>Setup time</td><td>~5 minutes (Intake only) · ~15 minutes (Bi-directional)</td><td></td></tr><tr><td>Prerequisites</td><td>Admin access to OneTrust and Lema</td><td></td></tr></tbody></table>

Lema supports two OneTrust connection modes. Choose the one that fits your workflow:

* **Intake only** — OneTrust sends vendor data to Lema via webhook whenever a new vendor is created. Simple, one-directional, no OAuth required.
* **Bi-directional** — Lema also pushes control gaps and assessment artifacts back into OneTrust as issues. Requires an additional OAuth client setup in OneTrust.

{% tabs %}
{% tab title="Intake only" %}
#### Integration steps

{% stepper %}
{% step %}
**Generate a webhook URL in Lema**

1. Go to **Integrations → + Add Integration → OneTrust (Intake)**.
2. Click **Generate Webhook URL** and copy the URL when it appears.

{% hint style="warning" %}
Save this URL immediately — it is shown only once.
{% endhint %}
{% endstep %}

{% step %}
**Configure the webhook in OneTrust**

1. In OneTrust, go to the **Integrations** tab and click **Add Integration**.
2. Select **Third Party Risk Management** as the integration type.
3. Under triggers, select **Inventory Vendor Created**.
4. Click **Add Action** and choose **HTTPS POST request**.
5. Paste your **Lema webhook URL** as the endpoint.
6. Set the request body to the following template:

```json
{
  "vendorName": "{{vendor.name}}",
  "vendorWebsite": "{{vendor.website}}",
  "vendorId": "{{vendor.id}}"
}
```

7. Click **Save & Activate**.
{% endstep %}
{% endstepper %}

From now on, every new vendor created in OneTrust will automatically appear in Lema.
{% endtab %}

{% tab title="Bi-directional" %}
#### Integration steps

{% stepper %}
{% step %}
**Generate client credentials in OneTrust**

1. In OneTrust, go to **Settings → Developer Portal** (or equivalent) and create a new **OAuth client**.
2. Assign the following scopes:
   * Inventory
   * Issue Management
   * Attachment
3. Copy the **Client ID** and **Client Secret**.
{% endstep %}

{% step %}
**Generate a webhook URL in Lema**

1. Go to **Integrations → + Add Integration → OneTrust (Bi-directional)**.
2. Click **Generate Webhook URL** and copy the URL.

{% hint style="warning" %}
Save this URL immediately — it is shown only once.
{% endhint %}
{% endstep %}

{% step %}
**Configure the OneTrust webhook**

1. In OneTrust, go to **Integrations → Webhooks** and add a new webhook.
2. Paste your **Lema webhook URL** as the endpoint.
3. Choose which events should trigger the webhook:
   * Vendor Created
   * Vendor Updated
   * Assessment Completed
4. Save and activate the webhook.
{% endstep %}

{% step %}
**Enable Issues Sync (optional)**

Turn on **Issues Sync** to push control gaps identified in Lema back into OneTrust as issues, and to have OneTrust status updates reflected in Lema.

1. In Lema's OneTrust integration settings, toggle on **Issues Sync**.
2. Map Lema control gap statuses to the corresponding OneTrust issue statuses.
{% endstep %}
{% endstepper %}

Once configured, vendor intake flows in from OneTrust and risk findings flow back out — giving your team a unified view across both platforms.
{% endtab %}
{% endtabs %}
