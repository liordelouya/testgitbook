---
description: >-
  Connect Google Workspace to pull device, user, and SaaS data into Lema
  automatically.
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

# Google Workspace

#### About the integration

<table><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Identity provider</td><td></td></tr><tr><td>Data collected</td><td>Devices, Users, SaaS data</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Google Workspace admin access · Google Cloud Console access</td><td></td></tr></tbody></table>

#### Integration steps

{% stepper %}
{% step %}
#### Create  a GCP service account

1. Go to **console.cloud.google.com** and create or select a project.
2. Navigate to **IAM & Admin → Service Accounts** and click **Create Service Account**.
3. Give it a name (e.g. "Lema Integration"), click **Create and Continue**, then **Done**.
{% endstep %}

{% step %}
#### Generate a credentials file

1. Click on the service account you just created.
2. Open the **Keys** tab and select **Add Key → Create New Key**.
3. Choose **JSON** format and click **Create**. The file downloads automatically — keep it handy.
{% endstep %}

{% step %}
#### Enable domain wide delegation

1. On the service account page, click **Show Advanced Settings** and copy the **Client ID**.
2. In your **Google Workspace Admin Console**, go to **Security → API Controls → Domain-wide Delegation → Add New**.
3. Paste the Client ID and add the following OAuth scopes:\
   `https://www.googleapis.com/auth/admin.reports.audit.readonly`\
   `https://www.googleapis.com/auth/admin.directory.user.readonly`\
   `https://www.googleapis.com/auth/admin.directory.group.readonly`
4. Click **Authorize**.
{% endstep %}

{% step %}
#### Enable the admin SDK API

1. In Google Cloud Console, go to **APIs & Services → Library**.
2. Search for **Admin SDK API** and click **Enable**.
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Google Workspace**.
2. Enter your **Google Workspace admin email address**.
3. Upload the **credentials.json** file from Step 2.
4. Click **Add Integration**.
{% endstep %}
{% endstepper %}

