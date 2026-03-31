---
description: >-
  Pull cloud resource inventory, IAM users, and infrastructure data from Google
  Cloud Platform into Lema.
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

# GCP (Google Cloud Platform)

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Identity Provider / Cloud Infrastructure</td><td></td></tr><tr><td>Data collected</td><td>Devices, Users, SaaS data</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes · ~1 minute if Google Workspace is already connected</td><td></td></tr><tr><td>Prerequisites</td><td>GCP organization admin access · Google Workspace admin access</td><td></td></tr></tbody></table>

{% hint style="success" %}
**Already connected Google Workspace?**\
Skip the entire setup — go to **Integrations → + Add Integration → GCP** and authorize using your existing credentials. Done in one click.
{% endhint %}

### Integration steps

{% stepper %}
{% step %}
#### Create a GCP service account

1. Go to **console.cloud.google.com** and create or select a project.
2. Navigate to **IAM & Admin → Service Accounts** and click **Create Service Account**.
3. Give it a descriptive name (e.g. `Lema Integration`), click **Create and Continue**, then **Done**.
{% endstep %}

{% step %}
#### Generate a credentials file

1. Click the service account you just created.
2. Open the **Keys** tab and select **Add Key → Create New Key**.
3. Choose **JSON** and click **Create** — the file downloads automatically.

{% hint style="warning" %}
Store this file securely. It grants delegated API access to your GCP organization and should never be committed to source control or shared externally.
{% endhint %}
{% endstep %}

{% step %}
#### Enable domain-wide delegation

1. On the service account page, click **Show Advanced Settings** and copy the **Client ID**.
2. In your **Google Workspace Admin Console**, go to **Security → API Controls → Domain-wide Delegation → Add New**.
3. Paste the Client ID and add the following OAuth scope:
   * `https://www.googleapis.com/auth/cloud-platform`
4. Click **Authorize**.
{% endstep %}

{% step %}
#### Enable required APIs

In Google Cloud Console, go to **APIs & Services → Library** and enable both:

* **Cloud Resource Manager API**
* **IAM API**
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → GCP**.
2. Enter your **Google Workspace admin email address**.
3. Upload the `credentials.json` file downloaded in Step 2.
4. Click **Add Integration**.
{% endstep %}
{% endstepper %}
