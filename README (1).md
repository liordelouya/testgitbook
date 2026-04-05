---
description: Get from zero to your first completed vendor assessment in Lema in minutes.
---

# Quickstart

{% stepper %}
{% step %}
### Invite your team

Go to **Settings → Users and Access** and invite the risk engineers, reviewers, and business owners who will participate in your TPRM program.

| Role       | Access                                                   |
| ---------- | -------------------------------------------------------- |
| **Admin**  | Full access including settings and integrations          |
| **Member** | Operational access to assessments, vendors, and findings |
| **Viewer** | Read-only access for stakeholders who need visibility    |

Learn more about [Users & access →](settings/users-and-permissions.md)
{% endstep %}

{% step %}
### Add your first third party

{% tabs %}
{% tab title="Manually" %}
Go to **Inventory → Third Parties** and click **+ Add Third-party**. Provide the company domain and basic profile details. Lema will enrich the profile automatically.
{% endtab %}

{% tab title="Via Intake portal" %}
Share the **Request Portal** with your business teams so they can submit new vendor requests directly. Submitted requests appear in the **Requests Queue** for a risk engineer to review and accept.
{% endtab %}

{% tab title="Via Integration" %}
Connect your procurement tools — such as Ramp, Zip and more.

Learn more about procurement [Integrations →](/broken/pages/ycZ7DfxZ0IBcicVScDkU)
{% endtab %}
{% endtabs %}

Learn more about [Adding a Third-party →](inventory/third-parties/adding-third-party.md)
{% endstep %}

{% step %}
### Complete the Inherent Risk Questionnaire

Open the vendor profile and open the **Inherent Risk** profile. Lema pre-populates the IRQ using AI-powered estimations based on the vendor's domain and profile data. Review each answer and confirm the inherent risk level.

{% hint style="warning" %}
The IRQ determines which scopes — and therefore which controls — activate in the assessment. Getting this right before starting is the single most important step in the workflow.
{% endhint %}

Learn more about [Inherent Risk →](inventory/third-parties/third-party-management/inherent-risk-profile.md)
{% endstep %}

{% step %}
### Start an assessment

Go to **Assessments** and click **+ New Assessment**. Select the vendor, then choose which projects should participate. Each project brings its own assessors and control scopes — scopes activate automatically based on the vendor's IRQ answers, so only relevant controls are included.

Learn more about [Starting an Assessment →](assessments/new-assessment.md)
{% endstep %}

{% step %}
### Review control outcomes

Once the assessment is open, Lema evaluates each in-scope control automatically against existing artifacts, integration data, and previous questionnaire responses.

Open the **Issues** tab to see:

* Controls already **validated** by Lema
* Controls with **gaps** that need attention
* Controls **waiting on evidence** from the vendor

Learn more about [Issues →](assessments/managing-assessment/issues.md)
{% endstep %}

{% step %}
### Request missing evidence

For controls that couldn't be validated automatically, send a **Smart Evidence Request** directly from the Issues tab.

Lema generates a targeted request listing exactly what's missing — not a generic questionnaire. The vendor receives a link to their portal to upload the required documents.

Learn more about [Smart Evidence Requests →](assessments/managing-assessment/issues.md)
{% endstep %}

{% step %}
### Conclude and share

Go to the **Conclusion** tab. Click **Generate AI Summary** to draft a narrative, review the control outcome breakdown, then issue your decision.

Once concluded, Lema automatically generates an **Executive Summary** ready to share with leadership, legal, or procurement.

Learn more about [Concluding an Assessment →](assessments/managing-assessment/concluding-assessment.md)
{% endstep %}
{% endstepper %}

### What's next?

{% columns %}
{% column %}
#### Control framework customization

Lema ships with a predefined control library. To customize the control framework to match your organization's standards, contact your Lema customer success representative.
{% endcolumn %}

{% column %}
#### Scopes customization

Configure rule-based scopes to control which assessments run for which vendors — based on inherent risk level and IRQ responses.

Scopes →
{% endcolumn %}

{% column %}
#### IRQ customization

Edit the Inherent Risk Questionnaire to capture the data signals that matter most to your program, and adjust per-answer risk levels to match your risk appetite.

Inherent Risk →
{% endcolumn %}
{% endcolumns %}
