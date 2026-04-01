---
description: >-
  Push procurement requests and vendor data from external systems directly into
  Lema
---

# Create/Update Third Party API

{% hint style="info" %}
### Prerequisites

* Access to a procurement system that can send webhooks
* Ability to manipulate the webhook request body
{% endhint %}

### Generate a Webhook URL

{% stepper %}
{% step %}
#### Open Integrations

Go to **Integrations** and click **+ Add Integration**, then select **Webhook**.
{% endstep %}

{% step %}
#### Name Your Integration

Provide an optional **Identifier** — used for internal management only.
{% endstep %}

{% step %}
#### Generate the URL

Click **Generate Webhook URL** and wait for the pop-up with the new URL.
{% endstep %}

{% step %}
#### Copy and Save

Click **Copy & Close** to copy the URL to your clipboard.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Store your webhook URL immediately.** This is the only time you can view and copy it. It cannot be retrieved later.
{% endhint %}

### Custom Fields

Custom fields allow you to pass additional structured data alongside the standard payload fields.

{% hint style="info" %}
To use custom fields, they must first be defined in Lema under **Settings → Custom Fields → Add Custom Field**.
{% endhint %}

**Supported types:** `text`, `date`, `multi-select`

#### Behavior

| Scenario                                    | Result                                           |
| ------------------------------------------- | ------------------------------------------------ |
| Sending a value                             | Overwrites any existing value for that field     |
| Sending an empty value                      | Not permitted — will not clear an existing value |
| Field name not pre-defined in Lema          | Value is ignored                                 |
| `multi-select` value not in predefined list | Value is ignored                                 |

### Processing Logic and Deduplication

When Lema receives a webhook payload, it checks whether to create a new record or update an existing one. Fields are evaluated in the following priority order:

<table><thead><tr><th width="120.2890625">Priority</th><th>Field</th></tr></thead><tbody><tr><td>1</td><td><code>requestId</code></td></tr><tr><td>2</td><td><code>vendorId</code></td></tr><tr><td>3</td><td><code>vendorWebsite</code></td></tr><tr><td>4</td><td><code>name</code></td></tr></tbody></table>

{% tabs %}
{% tab title="Existing Record" %}
If the `requestId` already exists, the payload **updates** that record.
{% endtab %}

{% tab title="New Record" %}
If the `requestId` is new or absent, Lema checks the remaining fields to **prevent duplicate entries** before creating a new record.
{% endtab %}
{% endtabs %}

#### Field Update Behavior

* **Immutable fields** — Core identification fields cannot be changed after a record is created. Subsequent payloads with new values for these fields are ignored.
* **Editable fields** — All other fields, including custom fields, are overwritten by the incoming value.

### Reference Values

{% tabs %}
{% tab title="Department Names" %}
`Legal` `IT` `Finance` `Security` `R&D` `HR` `Operations` `Sales` `Marketing` `Customer Success` `Product`
{% endtab %}

{% tab title="Vendor Status" %}
`Assessment Required` `In Assessment`
{% endtab %}

{% tab title="Vendor Lifecycle" %}
`Unsanctioned` `Onboarded` `In Evaluation` `Offboarded` `Archived`
{% endtab %}
{% endtabs %}
