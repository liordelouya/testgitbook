---
description: >-
  Connect Jira to track assessment findings as Jira issues, or use Jira as a
  procurement intake source to feed vendor records into Lema.
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

# Jira

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Issue Management · Procurement</td><td></td></tr><tr><td>Data collected</td><td>Jira issue IDs (Issue Management) · Vendor and procurement request data (Intake)</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Atlassian organization admin access</td><td></td></tr></tbody></table>

Lema supports two Jira connection modes. Choose the one that fits your workflow — or set up both:

* **Issue Management** — Lema creates and tracks Jira issues directly from assessment findings. Requires an API token.
* **Intake** — Jira acts as a procurement intake channel. When a Jira issue is created or transitioned, vendor data is automatically routed into Lema via webhook.

{% tabs %}
{% tab title="Issue Management" %}
### Integration steps

{% stepper %}
{% step %}
#### Create a dedicated Atlassian account

In your **Atlassian Admin console**, create either:

* A **service account** (recommended) — ideal for automation, not tied to a named employee
* A **user account** — the account that will own and manage Jira issues on Lema's behalf

Ensure this account has the appropriate project-level permissions in every Jira project you want Lema to interact with.
{% endstep %}

{% step %}
#### Generate an API token

1. Log in to the dedicated account and go to **id.atlassian.com → Security → API tokens**.
2. Click **Create API token**, give it a label (e.g. `Lema Integration`), and copy the generated token.

{% hint style="warning" %}
The token is shown only once. Copy it before closing this dialog.
{% endhint %}

Ensure the token has the following permission scopes:\
`read:jira-work` · `write:jira-work` · `read:jira-user`
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Jira (Issue Management)**.
2. Select your **Account Type** — **Cloud** or **Server**.
3. Enter your **Jira site domain** (e.g. `yourorg.atlassian.net`).
4. Enter the **Email** and **API Token** for the account created in Step 1.
5. Click **Add Integration**.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Intake" %}
### Integration steps

{% stepper %}
{% step %}
#### Generate a webhook URL in Lema

1. Go to **Integrations → + Add Integration → Jira (Intake)**.
2. Click **Generate Webhook URL** and copy the URL.

{% hint style="warning" %}
Save this URL immediately — it is shown only once.
{% endhint %}
{% endstep %}

{% step %}
#### Create a Global Automation rule in Jira

1. In Jira, go to **Settings → System → Global Automation** (or the Automation section within your project).
2. Create a new rule and set your trigger (e.g. **Issue Created** or **Issue Transitioned**).
3. Add an action: **Send Web Request**.
4. Set the URL to your **Lema webhook URL** and the method to **POST**.
5. Configure the request body to include the relevant issue fields — vendor name, website, requester, and any other fields you want mapped into Lema.
6. **Save** and **enable** the rule.

{% hint style="info" %}
You can create multiple automation rules with different triggers or project scopes — for example, one rule for new vendor requests and another for approved ones.
{% endhint %}
{% endstep %}
{% endstepper %}

Whenever a Jira issue matches your automation trigger, Lema will automatically create or update the corresponding vendor record.
{% endtab %}
{% endtabs %}
