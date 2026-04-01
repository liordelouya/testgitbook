---
description: >-
  Pull user directory, group memberships, and mail metadata from Gmail into Lema
  for visibility into communication patterns and access.
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

# Gmail

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Email</td><td></td></tr><tr><td>Data collected</td><td>Users, Groups, Mail Metadata</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Google Workspace admin access · Google Cloud Console access</td><td></td></tr></tbody></table>

{% hint style="info" %}
**Already connected Google Workspace?**\
You can reuse the same service account. Add the Gmail-specific OAuth scopes in Step 3 and enable the Gmail API in Step 4 — then skip straight to connecting in Lema.
{% endhint %}

### Integration steps

{% stepper %}
{% step %}
**Create a GCP service account**

1. Go to **console.cloud.google.com** and create or select a project.
2. Navigate to **IAM & Admin → Service Accounts** and click **Create Service Account**.
3. Give it a name (e.g. `Lema Gmail Integration`), click **Create and Continue**, then **Done**.
{% endstep %}

{% step %}
**Generate a credentials file**

1. Click the service account you just created.
2. Open the **Keys** tab and select **Add Key → Create New Key**.
3. Choose **JSON** and click **Create** — the file downloads automatically.

{% hint style="warning" %}
Store this file securely. It grants delegated API access to your Google Workspace environment and should never be committed to source control or shared externally.
{% endhint %}
{% endstep %}

{% step %}
**Enable domain-wide delegation**

1. On the service account page, click **Show Advanced Settings** and copy the **Client ID**.
2. In your **Google Workspace Admin Console**, go to **Security → API Controls → Domain-wide Delegation → Add New**.
3. Paste the Client ID and add the following OAuth scopes:
   * `https://www.googleapis.com/auth/gmail.metadata`
   * `https://www.googleapis.com/auth/admin.directory.user.readonly`
   * `https://www.googleapis.com/auth/admin.directory.group.readonly`
4. Click **Authorize**.
{% endstep %}

{% step %}
**Enable the Gmail API**

1. In Google Cloud Console, go to **APIs & Services → Library**.
2. Search for **Gmail API** and click **Enable**.
{% endstep %}

{% step %}
**Connect in Lema**

1. Go to **Integrations → + Add Integration → Gmail**.
2. Enter your **Google Workspace admin email address**.
3. Upload the `credentials.json` file downloaded in Step 2.
4. Click **Add Integration**.
{% endstep %}
{% endstepper %}
