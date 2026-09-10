---
title: External-facing Personal Data Rights form configuration
description: Privacy teams can tailor the external-facing Personal Data Rights \(PDR\) form per jurisdiction and data subject type. This customization allows them to control location specific content, authorized agent submission, and the available request types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-05-24"
reading_time_minutes: 2
breadcrumb: [Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# External-facing Personal Data Rights form configuration

Privacy teams can tailor the external-facing Personal Data Rights \(PDR\) form per jurisdiction and data subject type. This customization allows them to control location specific content, authorized agent submission, and the available request types.

Privacy laws give data subjects, such as customers and ex-employees, specific rights over their personal data that an organization collects. These can include right to access, correct, delete, or opt out of certain uses. The local laws determine which privacy rights data subjects can exercise, who is allowed to submit a request on their behalf, what disclosures must appear when a request is submitted, and the information the organization can collect at intake to process the request.

Without a configurable layer, organizations either present the same set of rights to every requester regardless of their location. This can mislead requesters about what's actually available to them under local law, or maintain several disconnected forms that are hard to keep current.

The external-facing PDR form gives data subjects a single public channel to submit requests. The configurable form enables privacy teams to adapt that channel, its content, available request types, authorized agent option, and other settings, to the jurisdiction and data subject type the requester selects.

\[Omitted image "ext-pdr-form-config.png"\] Alt text: Flowchart showing the steps to configure an external-facing PDR form record.

## Enabling language translation in the external-facing PDR form

The external-facing PDR form supports multiple languages. Most static field labels such as **Country** or **Request submitted by**, are hardcoded strings that are translated automatically when the corresponding language plugin is installed. For the list of available plugins and steps to activate one, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateALanguage.md).

However, custom form content that a PDR admin enters manually on the external form configuration record is specific to their organization, so the system doesn't translate it automatically. To provide your own translation for a field, create a new record in the Translated Text \[sys\_translated\_text\] table. For each language that you want the form to support, a separate record must be created. For steps, see .

For more information about how translations work across ServiceNow, including the Field Labels, Choices, and Messages tables, see [https://www.servicenow.com/community/itsm-forum/servicenow-localization-and-language-translation/m-p/3455929](https://www.servicenow.com/community/itsm-forum/servicenow-localization-and-language-translation/m-p/3455929).

-   **[Create a PDR external-facing form configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ext-form-record.md)**  
Create the parent external form configuration record that anchors all location, data subject type, and request type rules for the external-facing Personal Data Rights \(PDR\) form.
-   **[Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md)**  
Configure the jurisdictions, authorized agent option, and per-location URLs for the external-facing Personal Data Rights \(PDR\) form. These settings determine what requesters in each jurisdiction see based on their local privacy rules.
-   **[Configure the data subject types for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ds-types.md)**  
Specify which data subject types the external-facing Personal Data Rights \(PDR\) form offers in each location, so the form presents only the data subject types that local regulation supports.
-   **[Map request types to data subjects for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/map-request-type-to-ds.md)**  
Configure the request types available to each data subject type within a jurisdiction. When a requester selects a data subject type in the external-facing Personal Data Rights \(PDR\) form, only the request types scoped to it appear.
-   **[Translate external-facing Personal Data Rights form labels and values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/translate-pdr-form-text.md)**  
Add translation values for the configurable fields on the external-facing Personal Data Rights \(PDR\) form, so that text specific to your organization is correctly translated.

**Parent Topic:**[Configuring Personal Data Rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configuring-personal-data-rights.md)

