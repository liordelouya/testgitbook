---
description: >-
  Automatically route Vendr procurement requests into Lema for third-party risk
  assessment via webhook.
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

# Vendr

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Procurement</td><td></td></tr><tr><td>Data collected</td><td>Third-Parties (Procurement Requests, Documents)</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Vendr admin access to configure automations</td><td></td></tr></tbody></table>

This integration is **webhook-based**: Lema generates a webhook endpoint, and a Vendr automation forwards procurement step data to it automatically.

### Integration steps

{% stepper %}
{% step %}
#### Generate a webhook URL in Lema

1. Go to **Integrations → + Add Integration → Vendr**.
2. Optionally, enter a **Secret** to sign webhook payloads for added security.
3. Click **Generate Webhook URL** and copy the URL.

{% hint style="warning" %}
This URL is shown only once. Save it before navigating away.
{% endhint %}
{% endstep %}

{% step %}
#### Create a Vendr automation

1. In Vendr, navigate to **Automations** and click **Add Automation**.
2. Set the trigger to: **Step Status Changed → Ready**.
3. Add an action: **Send Webhook**.
4. Set the endpoint to your **Lema webhook URL**.
5. Set the payload body to:

```
{{ trigger.output.webhookEvent | json }}
```

6. Click **Turn On** to activate the automation.
{% endstep %}
{% endstepper %}

Whenever a procurement step becomes **Ready** in Vendr, the details will automatically sync into Lema.
