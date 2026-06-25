---
title: Operational Resilience release notes
description: The ServiceNow Operational Resilience application helps organizations maintain business services during adverse events, such as pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Operational Resilience release notes

The ServiceNow® Operational Resilience application helps organizations maintain business services during adverse events, such as pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Australia release.

## Operational Resilience highlights for the Australia release

-   Export Digital resilience incident reporting \(DRIR\) action tasks in Microsoft Word, Microsoft Excel, or JSON for regulatory reporting.
-   Run an advanced scenario analysis with guided steps for dependency mapping, statistical modeling, scenario testing, and impact review.
-   Generate consistent, regulator-ready reports using optional currency conversion and third-party expense aggregation in Digital Operational Resilience Act \(DORA\) Register of Information reporting.
-   Validate Legal Entity Identifiers \(LEIs\) in real time against the Global Legal Entity Identifier Foundation \(GLEIF\) API across record forms, CSV downloads, and Microsoft Excel uploads. Use the LEI Validation Report for compliance tracking.
-   Customize DRIR document outputs through Reporting and Template configuration modules.

See [Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-opres-landing-page.md) for more information.

**Important:** Australia is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Operational Resilience to Australia

Beginning with Operational Resilience release 22.0.x, the following scheduled jobs are deactivated for new installations by default:

-   **Calculate red flags for CSDM and dependencies**
-   **Update CSDM and other dependencies**

For existing installations, these jobs retain their current active or inactive state.

## New in the Australia release

-   **[Export action task reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/work-on-action-tasks.md)**

    Export DRIR assessment action task reports in Microsoft Word, Microsoft Excel, or JSON format from a drop-down menu. Generate Microsoft Word documents for narrative reports, Microsoft Excel spreadsheets with structured question-answer layouts, or JSON files for system integrations.

-   **[Create reporting configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reporting-configurations.md)**

    Manage document outputs centrally with the Reporting Configurations module in Digital resilience incident reporting. Administrators can manage template configurations, content configurations, and data relationship configurations from one place.

-   **[Convert and aggregate contractual expenses to regulator-required currencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/currency-conversion-aggregation.md)**

    Standardize annual expense values during Register of Information report generation by enabling optional currency conversion and third-party total expense aggregation. The application converts contract amounts to a base currency using 32 European Central Bank \(ECB\) exchange rates based on the reference date. Administrators upload monthly rates into the system. When eligibility criteria are met, expenses across multiple contracts are aggregated by third-party providers or engagements, generating consolidated reports that comply with DORA regulatory requirements.

-   **[Validate Legal Entity Identifiers using GLEIF API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-legal-entity.md)**

    Validate Legal Entity Identifiers \(LEIs\) in real time against the GLEIF API across all four record form types — Legal Entity, Branch, Third Party, and Third Party Engagement. Name and country fields are auto-populated or cross-checked on create and update, with warnings shown on mismatch.

    During Microsoft Excel upload, a batch verification consolidates and validates all LEIs against GLEIF before processing, flagging warnings while allowing administrators to save flagged rows for later correction. During CSV package download, a dedicated LEI validation report is generated.

-   **[GLEIF API performance using system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/properties-dora.md)**

    Configure GLEIF API behavior using the following system properties:

    -   **sn\_dora\_accel.gleif\_api\_batch\_size** — Controls how many LEIs are sent per request.
    -   **sn\_dora\_accel.gleif\_api\_timeout\_ms** — Sets the HTTP timeout per API call.
    -   **sn\_dora\_accel.lei\_save\_on\_gleif\_error** — Controls whether rows that fail GLEIF validation during Microsoft Excel upload are saved with warnings or rejected.
-   **[Monetary values for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/properties-dora.md)**

    Control monetary value precision in DORA reports using the **sn\_dora\_accel.decimals\_monetary** system property. Set it to 0 to round to whole units, or a negative value \(for example, -3\) to round to thousands, based on regulator requirements.

-   **Duplicate record detection and warnings in DORA reporting [Create Microsoft Excel download and upload request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

    Detect and prevent duplicate DORA records across key workflows. A business rule blocks saving on the Contractual Arrangement form when a duplicate record is detected. Warnings are displayed when duplicate rows are found during CSV downloads.

-   **[Run advanced scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md)**

    Plan and run advanced scenario analysis on a dedicated Scenario Analysis record, capturing simulation method, dependencies, and assignee. Progress through a guided Playbook with stages for dependency scoping, scenario testing, result review, impact assessment, and final completion.

    Execute statistical model profiles to evaluate severe-but-plausible scenarios across services and dependencies. The record is locked once the treatment decision and reason are recorded.

-   **[Template versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-sae-templates.md)**

    Track Smart Assessment Engine \(SAE\) template versions across assessment flows. New assessments automatically use the latest published Smart Assessment template version, while existing records on older versions continue to function without disruption. Assessment questions and automation logic handle different template versions correctly within the same flow.


## UI changes

-   **[Export action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/work-on-action-tasks.md)**

    The **Export** UI action on the action task form displays the following options: **Generate MS Word**, **Export Excel**, and **Export JSON**.

-   **[Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-excel-report-aggregate-expenses.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.x, the Excel download/upload request form includes the following fields for converting and aggregating contractual expenses to currencies required by regulators:

    -   **Report type**
    -   **Enable currency conversion**
    -   **Base currency**
    -   **Enable third-party total expense aggregation**
    -   **Reference date**
    -   **Date of the reporting**
    The **Type** field includes the **Plain-csv reporting package** option for generating reports in Comma-Separated Values \(CSV\) format.

    A business rule checks eight composite key fields when saving a contractual arrangement and displays a warning if a duplicate is found. B.05\_02 includes a link to open the duplicate record directly for comparison. B.05\_01 correctly includes ICT Intra-Group Service Provider \(Legal Entity providers\) in the ICT Third-Party Service Provider report.

    A warning is displayed when a Legal Entity Identifier \(LEI\) fails validation or a mismatch is detected against the GLEIF public API across all four record form types.

-   **[Create reporting configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reporting-configurations.md)**

    The Reporting Configurations module is provided in the Digital resilience incident reporting application to drive incident report generation.

-   **[Advanced scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md)**

    The **Playbook** tab is provided in the Scenario analysis records.

    The **Statistical Modelling** and **Manual** options are available in the **Method** field on the **Details** tab.

-   **[Template versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-sae-templates.md)**

    New assessments display the latest published Smart Assessment template version.


## Changed in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For more information, see [Install Operational Resilience application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/download-opres.md).

## Activation information

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-overview.md)**

    Use the ServiceNow® [Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-overview.md) application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce the reaction time from days to minutes.

-   **[Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/advanced-risk-assessment.md)**

    Use the ServiceNow®Advanced Risk application to identify, measure, and track risks. The application includes the workflows for risk assessments and events, confirming efficient management of your organization's risk profile.

-   **[Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_PolicyComplianceMgmt.md)**

    Use the ServiceNow®Policy and Compliance Management application to create and manage policies, standards, and internal control procedures that are mapped to external regulations and general guidelines.

-   **[Business Continuity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/business-continuity-mangmt-overview.md)**

    Use the ServiceNow®Business Continuity Management application to confirm that your organization can keep delivering products and services at an acceptable level even when faced with disruptive events.

-   **[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/avr-landing.md)**

    Use the ServiceNow®Vulnerability Response application to enable security users to analyze security data, implement changes, and generate security incidents.

-   **[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_IncidentManagement.md)**

    Use the ServiceNow®Incident Management application to restore normal service operation while minimizing the impact to business operations and maintaining quality.

-   **[Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sir-landing-page.md)**

    Use the ServiceNow®Security Incident Response application to manage the life cycle of your security incidents from the initial analysis to containment, eradication, and recovery.

-   **[Digital Operational Resilience Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-dg-resi-party-regi.md)**

    Use the ServiceNow®Digital Operational Resilience Management application for uploading and downloading all individual DORA tables. It’s automatically installed when the Digital Resilience Third-party Information Register is activated.

-   **[Data registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-360-deg-rel-vis.md)**

    Use the ServiceNow®Data registry application to explore the relationships between different types of critical data that affect your business, such as controls, risks, and issues, visually.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

