# Questionnaires

The Questionnaires tab is where you send structured information requests to the vendor. Use questionnaires when you need specific answers that can't be determined from artifacts alone — for example, asking a vendor to list all their sub-processors, describe their incident response process, or clarify a specific policy.

Questionnaire responses are shared through the Vendor Portal and count as artifacts — Lema uses them to re-evaluate controls once submitted.

### Sending a Questionnaire

{% stepper %}
{% step %}
### Add recipients and due date

Click **+ Recipients** to select the vendor contacts who should receive the questionnaire, and **Pick a date** to set a response deadline.
{% endstep %}

{% step %}
### Select a template

Click **+ Add questionnaire** and select one or more questionnaire templates from the dropdown. Templates are configured in Questionnaire Templates. Learn more about [questionnaire templates](../../settings/assessment-settings/questionnaires-templates.md)
{% endstep %}

{% step %}
### Publish

Click **Save** to publish the questionnaire. Recipients receive an email invitation with a link to the Vendor Portal where they can review and respond to each question.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
You can open the **Third-party portal** link in the top right to preview exactly what the vendor sees before publishing.
{% endhint %}

### Published Questionnaires

Once sent, questionnaires appear in the Published questionnaires list. You can track response status and see when the vendor has submitted their answers. Submitted responses are automatically analyzed by Lema and used to re-evaluate relevant controls.
