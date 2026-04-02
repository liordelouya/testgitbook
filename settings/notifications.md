---
description: Configure how and when Lema sends notifications
---

# Notifications

Configure how and when Lema sends notifications from **Settings → Notifications**. Settings are split across three tabs: **Third-party**, **Organization**, and **Personal**.

{% tabs %}
{% tab title="Third-party" %}
Controls automated email reminders sent to vendors for incomplete questionnaires and outstanding smart evidence requests.

**Ongoing reminders**

Set a recurring reminder cadence while a questionnaire or evidence request remains incomplete:

* Never
* Every 3 days
* Every 5 days
* Every 7 days

**Due date reminders**

Send a reminder 2 days before the due date. Enabled by default.
{% endtab %}

{% tab title="Organization" %}
Route Lema notifications to a shared Slack channel for your team.

Connect your Slack workspace, then select a public channel from the dropdown. All Lema platform notifications will be posted to that channel.

{% hint style="info" %}
After connecting Slack, invite the Lema app to your desired channel by typing `/invite @Lema` in that channel. The channel will then appear in the selection dropdown.
{% endhint %}
{% endtab %}

{% tab title="Personal" %}
Configure your individual notification preferences — which events you receive and how.

**Slack (personal)**

Connect Slack to receive Lema notifications as private direct messages from the SlackBot.

**Notification scope**

Choose which third parties you want to receive notifications for:

* **All third-parties** — notifications for all monitored vendors across your workspace
* **Only my third-parties and assessments** — notifications only for vendors and assessments where you are assigned as owner, assessor, or collaborator

**Notification triggers**

Select which events trigger a notification and through which channel (Slack or Email). Trigger settings apply to the scope selected above.

| Category                   | Event                                                                                                               |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Third-party**            | Inherent Risk Updated, Status Updated, Business Owner Intake Submission                                             |
| **Finding**                | New Comment, Severity Updated, Status Updated, Finding Detected                                                     |
| **Questionnaire**          | Questionnaire Completed, Questionnaire Deleted, New Comment Added, Questionnaire Submitted, New Questionnaire Added |
| **Smart evidence request** | Comments Added                                                                                                      |
| **Assessment reminders**   | 2 days before due date                                                                                              |

{% hint style="info" %}
Slack triggers are only available after connecting your personal Slack account in the Channels section above.
{% endhint %}
{% endtab %}
{% endtabs %}
