# Table of contents

## Get Started

* [Quick Start](get-started/quick-start.md)
* [Concepts](get-started/concepts.md)

## Intake

* [Third-Party Request Portal](intake/third-party-request-portal.md)
* [Requests Queue](intake/requests-queue.md)
* [Procurement Integrations](intake/procurement-integrations/README.md)
  * [Jira](intake/procurement-integrations/jira.md)
  * [Coupa](intake/procurement-integrations/coupa.md)
  * [Zip](intake/procurement-integrations/zip.md)
  * [Asana](intake/procurement-integrations/asana.md)
  * [Ramp](intake/procurement-integrations/ramp.md)
  * [Vendr](intake/procurement-integrations/vendr.md)
  * [OneTrust](intake/procurement-integrations/onetrust.md)
  * [Graphite Connect](intake/procurement-integrations/graphiteconnect.md)
  * [LogicManager](intake/procurement-integrations/logicmanager.md)

## Inventory

* [Third Parties](inventory/third-parties/README.md)
  * [Adding a Third Party](inventory/third-parties/adding-third-party.md)
  * [Third-Party Affiliates](inventory/third-parties/third-party-affiliates.md)
  * [Engagements](inventory/third-parties/third-party-engagements.md)
  * [Third-Party Profile](inventory/third-parties/third-party-management/README.md)
    * [Inherent Risk Profile](inventory/third-parties/third-party-management/inherent-risk-profile.md)
    * [Assessments](inventory/third-parties/third-party-management/assessments.md)
    * [Controls](inventory/third-parties/third-party-management/controls.md)
    * [Findings](inventory/third-parties/third-party-management/findings.md)
    * [Artifacts](inventory/third-parties/third-party-management/artifacts.md)
    * [Assets](inventory/third-parties/third-party-management/assets.md)
    * [Permissions](inventory/third-parties/third-party-management/permissions.md)
    * [Usage](inventory/third-parties/third-party-management/usage.md)
* [Fourth Parties](inventory/fourth-parties.md)

## Assessments

* [Assessments Directory](assessments/assessments-directory.md)
* [Starting an Assessment](assessments/new-assessment.md)
* [Vendor Portal](assessments/vendor-portal.md)
* [Managing an Assessment](assessments/managing-assessment/README.md)
  * [Overview](assessments/managing-assessment/overview.md)
  * [Questionnaires](assessments/managing-assessment/questionnaires.md)
  * [Controls](assessments/managing-assessment/controls.md)
  * [Issues](assessments/managing-assessment/issues.md)
  * [Artifacts](assessments/managing-assessment/artifacts.md)
  * [Concluding an Assessment](assessments/managing-assessment/concluding-assessment.md)

## Monitoring

* [Agentic Risk Engineer](monitoring/agentic-risk-engineer.md)
* [Findings](monitoring/findings.md)

## Analytics

* [Risk](analytics/risk.md)
* [Business](analytics/business.md)
* [Efficiency](analytics/efficiency.md)

## Integrations

* [Identity Providers](integrations/identity-providers/README.md)
  * [Okta](integrations/okta.md)
  * [Microsoft Entra ID](integrations/microsoft-entra-id.md)
* [Google](integrations/google/README.md)
  * [Google Workspace](integrations/google-workspace.md)
  * [Gmail](integrations/gmail.md)
  * [Google Drive](integrations/google-drive.md)
  * [GCP (Google Cloud Platform)](integrations/gcp-google-cloud-platform.md)
* [Cloud Security](integrations/cloud-security/README.md)
  * [Wiz](integrations/wiz.md)
  * [Netskope](integrations/netskope.md)

## Settings

* [Users & Permissions](settings/users-and-permissions.md)
* [SSO](settings/sso.md)
* [Notifications](settings/notifications.md)
* [Third-Party Settings](settings/third-party-settings/README.md)
  * [Inherent Risk](settings/third-party-settings/inherent-risk.md)
  * [Custom Fields](settings/third-party-settings/custom-fields.md)
* [Assessment Settings](settings/assessment-settings/README.md)
  * [Scopes](settings/assessment-settings/scopes.md)
  * [Cadence](settings/assessment-settings/cadance.md)
  * [Controls](settings/assessment-settings/controls.md)
  * [Questionnaire Templates](settings/assessment-settings/questionnaires-templates.md)
  * [Summary Template](settings/assessment-settings/summary-template.md)

## API Reference

* [Create/Update Third Party API](README.md)
  * ```yaml
    type: builtin:openapi
    props:
      models: true
      downloadLink: false
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: update-vendor
    ```
* [Get Third Parties API](api-reference/get-third-parties-api/README.md)
  * ```yaml
    type: builtin:openapi
    props:
      models: true
      downloadLink: false
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: get-companies
    ```
