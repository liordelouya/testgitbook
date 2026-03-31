---
description: >-
  Pull vendor profiles, company details, and shared artifacts from
  GraphiteConnect into Lema.
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

# GraphiteConnect

### About the integration

<table><thead><tr><th width="160"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td>Category</td><td>Supplier Management</td><td></td></tr><tr><td>Data collected</td><td>Vendors, Company Details, Artifacts</td><td></td></tr><tr><td>Setup time</td><td>~10 minutes</td><td></td></tr><tr><td>Prerequisites</td><td>GraphiteConnect account with API key permissions</td><td></td></tr></tbody></table>

### Integration steps

{% stepper %}
{% step %}
#### Create an API key

1. Log in to **GraphiteConnect** and click your **profile icon** in the top right.
2. Go to **Settings → API Keys**.
3. Click **Create API Key**, give it a name (e.g. `Lema Integration`), and copy the generated key.
{% endstep %}

{% step %}
#### Connect in Lema

1. Go to **Integrations → + Add Integration → GraphiteConnect**.
2. Paste in your **API Key**.
3. Click **Add Integration**.
{% endstep %}
{% endstepper %}
