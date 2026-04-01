---
description: Let business users across your organization submit vendor requests
---

# Third-Party Request Portal

The Request Portal is a standalone web form that lets business users across your organization submit vendor requests directly to the TPRM team — no procurement system required.

When a business user submits a request, it lands in your [Requests Queue](requests-queue.md) for triage. No vendor record is created until the TPRM team approves it.

{% hint style="info" %}
The portal is designed for organizations that want an independent, TPRM-owned intake process — separate from procurement tools.
{% endhint %}

## How It Works

{% stepper %}
{% step %}
### Share the portal link

Copy the portal link from the Intake Builder and distribute it to your internal stakeholders. Access is restricted to approved email domains — only users authenticating with an allowed domain can submit a request.
{% endstep %}

{% step %}
### Business user submits a request

The requester authenticates via OTP, fills out the form, and submits. All mandatory fields must be completed before submission is allowed.

After submitting, they receive a confirmation with a unique **Request ID** and a message that the TPRM team will be in touch.
{% endstep %}

{% step %}
### Request lands in the queue

The submission appears in the [Requests Queue](requests-queue.md). The TPRM team is notified via email or Slack. From there, the risk engineer triages, approves, or rejects the request.
{% endstep %}
{% endstepper %}

## Default Form Sections

The portal ships with a default template. Every submission includes:

| Section                                       | What it captures                                                       |
| --------------------------------------------- | ---------------------------------------------------------------------- |
| **Third-Party Company Information**           | Vendor name (auto-complete), website URL                               |
| **Scope of Service & Engagement Details**     | Engagement type, name, description                                     |
| **Business Relationship & Points of Contact** | Business owner, vendor point of contact                                |
| **Security, Privacy & Resiliency Assessment** | IRQ questions — data types, permissions, business impact, integrations |

{% hint style="info" %}
**The intake form is your first IRQ signal.** The Security, Privacy & Resiliency Assessment section is synced directly with your IRQ template. Answers submitted by the business user automatically pre-populate the vendor's Inherent Risk Profile — so your risk scoring starts with real business context, not guesswork.

This section is managed in your global IRQ settings. You can hide specific questions from the intake form to keep it concise, but changes to the question set must be made there.
{% endhint %}

## IRQ Mapping & Inherent Risk Pre-population

When a request is approved, answers from the **Security, Privacy & Resiliency Assessment** section automatically fill the vendor's Inherent Risk Profile.

This means the TPRM team gets a head start — the business owner who requested the vendor has already answered what data is shared, what permissions are needed, and what the operational impact would be.

In the Inherent Risk Profile, you'll see each field clearly tagged by its data source:

* **Business intake** — answered by the requester
* **AI projection** — Lema's automated estimate
* **Final selection** — the value your team confirmed

{% hint style="warning" %}
Intake auto-fill and AI auto-fill are mutually exclusive. If intake data is applied, AI auto-fill is disabled until you clear the existing values.
{% endhint %}

## Configuring the Portal

Open **Settings → Intake Builder** to customize the form.

**What you can do:**

* Add, remove, and reorder sections and questions
* Set questions as mandatory or optional
* Add conditional logic (show a question based on a previous answer)
* Map questions to existing vendor or engagement custom fields
* Add custom questions for internal context (not mapped to any Lema data point)
* Upload your logo and set section descriptions

**What's locked:**

* Core fields (vendor name, submitting person, request title) cannot be removed
* IRQ section questions can be hidden but not deleted from this form

## Managing Access

Control who can access the portal from the Intake Builder.

* **Domain allowlist** — Restrict submissions to specific company domains (e.g., `yourcompany.com`). Multiple domains are supported.
* **Copy link** — The portal has a single shareable link. It updates whenever you save changes to the template.

{% hint style="warning" %}
The sharing link is disabled while you're in edit mode. Save your changes first, then copy and share the link.
{% endhint %}

## After Submission

Business users receive:

* An email confirmation with their Request ID
* An email notification when their request is approved or rejected (rejections include a note from the TPRM team)

TPRM team receives:

* An email or Slack notification for each new submission

The submitted request is visible in the [Requests Queue](requests-queue.md).
