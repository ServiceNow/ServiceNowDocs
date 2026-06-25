---
title: Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes
description: The ServiceNow Operational Sustainability Management application \(formerly known as Environmental, Social, and Governance Management\) manages sustainability-related data, metrics, and reporting requirements. Operational Sustainability Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes

The ServiceNow® Operational Sustainability Management application \(formerly known as Environmental, Social, and Governance Management\) manages sustainability-related data, metrics, and reporting requirements. Operational Sustainability Management was enhanced and updated in the Australia release.

## Operational Sustainability Management highlights for the Australia release

-   Edit calculated metric definition formulas after execution and apply updated formulas from a specific date, preserving historical data integrity with formula versioning.
-   The Microsoft 365 reporting add-in and the Document designer add-in are consolidated into a single Document designer plugin for streamlined sustainability reporting.
-   Use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word.
-   Map Operational Sustainability Management roles to Risk Library and Compliance Library feature roles to control access to risk and compliance data based on functional domains.
-   Perform CSRD-compliant double materiality assessments in Socialsuite and automatically sync the results with the Operational Sustainability Management application.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md) for more information.

**Important:** Operational Sustainability Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Edit a calculated metric definition formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/edit-a-calculated-metric-definition-formula.md)**

    After upgrading GRC: Metrics to version 22.3.1, you can edit a calculated metric definition formula after it has been executed. When you save an edited formula, select a date from which the updated formula applies. Each saved edit creates a new formula version.

-   **[Microsoft Word based audit report templates using Document designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/document-designer-template.md)**

    After upgrading Document Designer to version 22.3.2, the Microsoft 365 reporting and Document Designer add-ins are consolidated into a single Document Designer plugin. A Create Claim button is added to the manifest. The repeater limit per document increases from 2 to 5, and the repetition limit per repeater increases from 200 to 500.

-   **[AI reporting assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-reporting-assistant.md)**

    After upgrading AI for Document Designer to version 22.3.3, you can use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word. The assistant inserts the output into your document as stories, tables, charts, or data points.

-   **[Components installed with Operational Sustainability Management \(formerly ESG Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/components-installed-with-esg.md)**

    After upgrading Operational Sustainability Management to version 22.3.1, Operational Sustainability Management roles are mapped to Risk Library and Compliance Library feature roles to enforce functional domain separation. Users assigned these roles can access only risk and compliance records tagged to the functional domains they are authorized for.

-   **[Document intelligence for utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/ai-driven-document-intelligence-for-utility-invoices.md)**

    After upgrading Now Assist for Operational Sustainability Management to version 22.0.1, unit values from invoices and updates metric data are extracted automatically, reducing manual data entry and improving data accuracy.

-   **[Integrating Operational Sustainability Management with Socialsuite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/integrate-operational-sustainability-with-SocialSuite.md)**

    After upgrading Operational Sustainability Management to version 22.0.1, streamline sustainability reporting and compliance processes by conducting CSRD-compliant double materiality assessments in Socialsuite and automatically syncing the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following Global Reporting Initiative \(GRI\) and European Sustainability Reporting Standards \(ESRS\) standards.

-   **[Create a threshold for a metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-threshold-for-a-metric.md)**

    After upgrading Operational Sustainability Management to version 22.0.1, you can configure thresholds with multiple levels and ranges for granular monitoring. When thresholds are breached, automated actions trigger immediately.


## Changed in this release

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
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Deprecated features

The ServiceNow Reporting manifest is deprecated. Use the Document Designer manifest for all reporting needs. Enhancements will be available on the Document Designer manifest only.

## Activation information

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **[Components installed with Operational Sustainability Management \(formerly ESG Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/components-installed-with-esg.md)Renamed or changed plugins**

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

