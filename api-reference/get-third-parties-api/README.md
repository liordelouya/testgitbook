---
description: Use the Lema Companies API to retrieve all vendors for your organization
---

# Get Third Parties API

{% hint style="info" %}
#### Prerequisites

* An access key issued by Lema (contact Lema support to obtain one)
{% endhint %}

#### **Endpoint output**

1. Name
2. Risk level
3. Vendor sources
4. Contacts
5. Tags
6. Custom fields
7. Re-assessment date

#### Authentication

Lema uses a two-step authentication flow. Your long-lived access key is exchanged for a short-lived session JWT, which is then passed as a Bearer token on all API requests.
