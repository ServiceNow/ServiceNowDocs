---
title: Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes
description: The ServiceNow Operational Sustainability Management application \(formerly known as Environmental, Social, and Governance Management\) manages sustainability-related data, metrics, and reporting requirements. Operational Sustainability Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes

The ServiceNow® Operational Sustainability Management application \(formerly known as Environmental, Social, and Governance Management\) manages sustainability-related data, metrics, and reporting requirements. Operational Sustainability Management was enhanced and updated in the Australia release.

## Operational Sustainability Management highlights for the Australia release

-   ServiceNow Otto is the new name for the Now Assist experience in Operational Sustainability Management. All Now Assist references have been updated to ServiceNow Otto.
-   You can group manual, calculated, and automated metrics into a campaign by entity, group, or both. When bulk actions are enabled, you can move an entire campaign through its lifecycle as a single unit, instead of tracking each metric independently.
-   Set a variance base value for a metric, so percentage-based threshold calculations stay meaningful even without prior-period data or if the previous value is zero.
-   Edit calculated metric definition formulas after execution and apply updated formulas from a specific date, preserving historical data integrity with formula versioning.
-   Use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word.
-   Perform CSRD-compliant double materiality assessments in Socialsuite and automatically sync the results with the Operational Sustainability Management application.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md) for more information.

**Important:** Operational Sustainability Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Operational Sustainability Management to Australia

To use campaigns, activate the following system properties:

-   sn\_esg.metric\_campaign: Enables campaigns on the Operational Sustainability Management workspace.
-   sn\_esg.campaign\_bulk\_action\_enabled: Enables bulk submission, approval, and rejection for campaigns.
-   sn\_esg.metric\_approval: Sets the approval mode for campaigns. Set the value to Simple for a single data owner and approver, or Advanced for multi-level approval chains.

## New in the Australia release

-   **[Campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/campaigns.md)**

    After upgrading GRC: Metrics to version 22.5.2, you can group manual, calculated, and automated metrics into a campaign by entity, by group, or both. The unique combination of Group, Frequency, Calendar type, and Entity defines each campaign's metric set. When bulk actions are enabled, the campaign moves through different states as a single unit. Each measurement period generates a campaign cycle that tracks Data collection, Approval, and Closed states for every metric in the campaign together, instead of each metric progressing independently.

-   **[Configure data owner and approver assignments for a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configure-data-owner-and-approver-assignments-for-a-campaign.md)**

    Configure data owner and approver assignments for a campaign from a single page. Submit, approve, or reject every task in a campaign cycle together instead of working through tasks one at a time.

-   **[Edit a calculated metric definition formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/edit-a-calculated-metric-definition-formula.md)**

    After upgrading GRC: Metrics to version 22.3.1, you can edit a calculated metric definition formula after it has been executed. When you save an edited formula, select a date from which the updated formula applies. Each saved edit creates a new formula version.

-   **[Microsoft Word based audit report templates using Document designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/document-designer-template.md)**

    After upgrading Document Designer to version 22.3.2, the Microsoft 365 reporting and Document Designer add-ins are consolidated into a single Document Designer plugin. A Create Claim button is added to the manifest. The repeater limit per document increases from 2 to 5, and the repetition limit per repeater increases from 200 to 500.

-   **[AI reporting assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-reporting-assistant.md)**

    With AI for Document Designer, you can use the AI reporting assistant to generate report content from ServiceNow data using prompts directly within Microsoft Word. The assistant inserts the output into your document as stories, tables, charts, or data points.

-   **[Components installed with Operational Sustainability Management \(formerly ESG Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/components-installed-with-esg.md)**

    After upgrading Operational Sustainability Management to version 22.3.1, Operational Sustainability Management roles are mapped to Risk Library and Compliance Library feature roles to enforce functional domain separation. Users assigned these roles can access only risk and compliance records tagged to the functional domains they are authorized for.

-   **[Document intelligence for utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/ai-driven-document-intelligence-for-utility-invoices.md)**

    After upgrading ServiceNow Otto for Operational Sustainability Management to version 22.0.1, unit values from invoices and updates metric data are extracted automatically, reducing manual data entry and improving data accuracy.

-   **[Integrating Operational Sustainability Management with Socialsuite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/integrate-operational-sustainability-with-SocialSuite.md)**

    After upgrading Operational Sustainability Management to version 22.0.1, streamline sustainability reporting and compliance processes by conducting CSRD-compliant double materiality assessments in Socialsuite and automatically syncing the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following Global Reporting Initiative \(GRI\) and European Sustainability Reporting Standards \(ESRS\) standards.

-   **[Create a threshold for a metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-threshold-for-a-metric.md)**

    After upgrading Operational Sustainability Management to version 22.0.1, you can configure thresholds with multiple levels and ranges for granular monitoring. When thresholds are breached, automated actions trigger immediately.


## UI changes

-   **[Campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/campaigns.md)**

    The Campaigns list and record views were added to the Operational Sustainability Workspace. Related lists for entities, metrics, campaign tasks, owners, and approvers are included, along with declarative Add/Remove actions for managing campaign entities and metrics.


## Changed in this release

-   **[Metric definition setting record fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/metric-definition-setting-record-fields.md)**

    After upgrading GRC: Metrics to version 22.5.2, Metric definitions now support a configurable variance base value, resolved from the individual metric, its metric definition, or a global default. Variance percentages remain meaningful when a previous-period value is missing or zero.


-   **[ServiceNow Otto® name announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

    The Now Assist for IRM \(sn\_irm\_gen\_ai\) plugin, which provides generative AI capabilities for RCM, has been renamed to ServiceNow Otto for IRM.


-   **[Components installed with Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/components-installed-with-grc.md)**

    After upgrading Operational Sustainability Management to version 22.3.1, role inheritance is updated to restrict access only to the resources required for each role. These changes apply to new installations only.

    -   The connection\_admin role is removed from sn\_esg.integration\_admin inheritance.
    -   The workspace\_user role is removed from Formula Builder configuration table access and from sn\_esg.reader and sn\_esg.data\_owner inheritance.
    -   The sn\_align\_core.ap\_read\_only role in sn\_esg.reader is replaced with sn\_ppm.reader.
    -   Read access to the sn\_esg\_gen\_ai\_emission\_calculation\_guidelines table is restricted to sn\_esg\_gen\_ai.cmd\_agent\_user.
    -   Metric reader access to Sustainable IT tables is restricted to required configuration tables only.
-   **[Configure templates for Document Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-template-for-document-designer.md)**

    After upgrading Operational Sustainability Management to version 22.3.2, the Business domain field in the Template configuration and Data relationship tables now references the GRC business domain \(sn\_grc\_business\_domain\). Previously, these fields referenced the M365 business domain.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Deprecated features

The ServiceNow Reporting manifest is deprecated. Use the Document Designer manifest for all reporting needs. Enhancements will be available on the Document Designer manifest only.

## Activation information

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Plugin information

-   **[Renamed or changed plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/components-installed-with-esg.md)**

    Microsoft 365 for ServiceNow Reporting \(sn\_esg\_msoff\_intg\): The Microsoft 365 reporting add-in is converted to a development plugin and is no longer available in the plugin installation UI. Document Designer is now a dependency of Operational Sustainability Management.

    The following plugins were renamed in the Australia release:

    -   Environmental, Social, and Governance Management \(com.sn\_esg\): Renamed Operational Sustainability Management \(com.sn\_esg\)
    -   ESG integration with Concur \(com.sn\_esg\_concur\): Renamed Operational Sustainability Integration with Concur \(com.sn\_esg\_concur\)
    -   ESG integration with DEX \(com.sn\_esg\_dex\_intg\): Renamed Operational Sustainability Integration with DEX \(com.sn\_esg\_dex\_intg\)
    -   ESG Regenerative finance \(com.sn\_esg\_refi\): Renamed Regenerative Finance for Operational Sustainability \(com.sn\_esg\_refi\)
    -   ESG Risk Management \(com.sn\_esg\_risk\_mgmt\): Renamed Operational Sustainability Risk Management \(com.sn\_esg\_risk\_mgmt\)
    -   Materiality Assessment \(com.sn\_osm\_ma\): Renamed Operational Sustainability Integration with Socialsuite \(com.sn\_osm\_ma\)
    -   Now Assist for Environmental, Social, and Governance \(ESG\) \(com.sn\_esg\_gen\_ai\): Renamed Now Assist for Operational Sustainability \(com.sn\_esg\_gen\_ai\)
    -   Urjanet ESG integration \(com.sn\_esg\_urjanet\): Renamed Operational Sustainability Integration with Urjanet \(com.sn\_esg\_urjanet\)
    -   Watershed integration for ESG \(com.sn\_esg\_watershed\): Renamed Operational Sustainability Integration with Watershed \(com.sn\_esg\_watershed\)
    -   Workday ESG integration \(com.sn\_esg\_workday\): Renamed Operational Sustainability Integration with Workday \(com.sn\_esg\_workday\)

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

