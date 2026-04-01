# Requests Queue

The Requests Queue is your central triage hub for all incoming vendor requests — whether they come from the [Third-Party Request Portal](third-party-request-portal.md), a connected procurement system (Zip, Jira, Coupa, etc.), or a webhook integration.

Every request lands here first. No vendor record is created and no data is pushed to your inventory until your team reviews and acts on it.

{% hint style="info" %}
The Requests Queue only appears if you have at least one active intake integration or the Request Portal configured. If you don't see it in the navigation, check your integrations in Settings.
{% endhint %}

## What's in the Queue

Each request row shows: source, third-party name, request title, requester, department, and submission date. By default, the queue shows pending requests sorted by submission date, newest first.

Use the filters to cut through the noise:

- **Source** — filter by procurement tool, webhook, or Lema portal
- **Third-Party** — narrow to a specific vendor
- **Request type** — New purchase, Renewal, or Scope change
- **Requester / Business owner / Data types** — further segmentation

Requests stay in the queue until you act on them. They do not auto-approve or auto-create vendor records.

## Reviewing a Request

Click any row to open the request drawer. It shows:

- **Request ID** and submission timestamp
- **Matched third-party** — Lema auto-matches the request to a vendor in your inventory using vendor finder logic. If the match is wrong, you can correct it before proceeding.
- **Inherent risk** and lifecycle status of the matched vendor
- **Engagements** linked to the vendor
- **Request details** — description, requester, department, spend, contract period, point of contact, artifacts
- **Source link** — jump directly to the original request in the procurement tool

{% hint style="info" %}
Procurement data is often incomplete or mismatched. You can edit and correct fields directly in the drawer before accepting — this is intentional. The queue is your quality gate before anything hits your inventory.
{% endhint %}

## Accepting a Request

When you accept a request, what happens next depends on whether the vendor already exists in your inventory.

{% tabs %}
{% tab title="New vendor" %}
Lema prompts you to create a vendor record. It pre-fills the profile using data from the request (business owner, point of contact, inherent risk inputs, artifacts). You can correct the suggested vendor name and details before confirming.

From there you can:
- **Start an assessment** — opens the assessment setup flow
- **Add to inventory without assessment** — creates the vendor record and closes the request
{% endtab %}

{% tab title="Existing vendor" %}
The request is linked to the matched vendor. Lema prompts you to start an assessment if one is needed. Request data (artifacts, contacts, IR inputs) is synced to the vendor profile.

You can also:
- **Close without assessment** — if the vendor is already assessed and no new review is needed
{% endtab %}

{% tab title="Affiliated third-party" %}
If the request is for a subsidiary or a standalone product that requires its own separate assessment, you can map it as an **Affiliated Third-Party** — linking it to a parent vendor while keeping it independently assessed.

See [Third-Party Affiliates](../inventory/third-parties/third-party-affiliates.md) for more on parent-child relationships.
{% endtab %}
{% endtabs %}

## Rejecting a Request

Click **Reject** in the drawer to decline the request. You can include a note — it will be sent to the requester by email.

Rejected requests move out of the active queue. You can view them under the **Archived** tab.

## Requests on the Vendor Profile

Once accepted, a request is permanently linked to the vendor. You can see all requests — past and present, from any source — in the **Requests tab** of the vendor's profile in inventory. This gives you a full audit trail of every intake event associated with that vendor.
