---
description: >-
  Connect Microsoft Entra ID to pull user, application, and delegated permission
  data into Lema.
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

# Microsoft Entra ID

### About the integration



<table><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Data collected</td><td>Administrative units, Applications, Delegated permissions, Users</td><td></td></tr><tr><td>Setup time</td><td>~15 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>Global Administrator or Application Administrator role in Azure</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Register an application in Azure

1. Sign in to the **Azure portal** and go to **Microsoft Entra ID → App registrations**.
2. Click **New registration**, give your app a name (e.g. "Lema Integration"), and click **Register**.
3. Copy the **Application (client) ID** and **Directory (tenant) ID** — you'll need both later.
{% endstep %}

{% step %}
#### Create a client secret

1. Go to **Certificates & secrets → Client secrets → New client secret**.
2. Add a description and set an expiration period, then click **Add**.
3. Copy the **Secret Value** immediately.

{% hint style="warning" %}
The Secret Value is shown only once. If you navigate away before copying it, you'll need to create a new secret.
{% endhint %}
{% endstep %}

{% step %}
#### Add API permissions and grant admin consent

1. Go to **API permissions → Add a permission → Microsoft Graph → Application permissions**.
2. Add:&#x20;

`AdministrativeUnit.Read.All`

`Application.Read.All`

`DelegatedPermissionGrant.Read.All`

`User.Read.All`

3. Click **Grant admin consent** and confirm.
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → Microsoft Entra ID**.
2. Enter your **Application (client) ID**, **Directory (tenant) ID**, and **Secret Value**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}







