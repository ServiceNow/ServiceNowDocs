---
title: Combined Operational Resilience release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Operational Resilience from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-operationalresilience-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Operational Resilience release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Operational Resilience from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Resilience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Resilience to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

After upgrading to Operational Resilience version 21.0.x, rerun the **Update CSDM and other dependencies** scheduled job to populate the additional metadata that was introduced in this release.

</td></tr><tr><td>

Australia

</td><td>

Beginning with Operational Resilience release 22.0.x, the following scheduled jobs are deactivated for new installations by default:

-   **Calculate red flags for CSDM and dependencies**
-   **Update CSDM and other dependencies**

For existing installations, these jobs retain their current active or inactive state.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Operational Resilience.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Measure resilience metrics using the CSDM model](https://www.servicenow.com/docs/access?context=using-csdm-v5&family=yokohama&ft:locale=en-US)**

Define the entity types and pillars in Operational Resilience and generate the entities. Establish relationships between CSDM objects, including business services, service offerings, business processes, and application services. Specify the type of main node configuration that you want to use by setting the **sn\_oper\_res.opres\_csdm\_main\_node\_config** property.

After generating the entities and setting up the main node configurations, you can import CMDB data into Operational Resilience for reporting. CSDM and their dependencies are updated weekly while the red flags data is calculated daily. The outcome is displayed on the Homepage or in the related list of the CSDM objects.

-   **[Specify the primary origin of an operational vulnerability](https://www.servicenow.com/docs/access?context=add-impacted-area-to-vul&family=yokohama&ft:locale=en-US)**

Identify the primary origin of an operational vulnerability in its record. Once the primary origin is specified, its upstream dependencies are automatically included in the impacted areas, enabling you to view the operational vulnerability from all affected perspectives.

-   **[Using Digital resilience incident reporting](https://www.servicenow.com/docs/access?context=drir-module&family=yokohama&ft:locale=en-US)**

Assess whether any critical services are affected and classify the reported incident as a major incident if necessary. Notify regulators of major incidents, categorized by their severity and security ratings.

The Digital resilience incident reporting module, accessible from the Operational Resilience Workspace, is integrated with Incident Management and Security Incident Response to generate and share reports in the format that is specified by the regulators.

You can generate an initial report within 24 hours, an intermediate report within 72 hours, and a final report within 1 month. All of these reports are automatically triggered by the application from the time that the incident is classified as a major incident.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Use the interactive Node Map visualization](https://www.servicenow.com/docs/access?context=configure-nexus-map-configurations&family=zurich&ft:locale=en-US)**

Navigate operational dependencies using the interactive Node map visualization. Configure node and edge settings in the Nexus map, then display Main node configurations directly within the Operational Resilience Workspace. The **Resilience map** action provides access to relationships for Business Services \(BS\), Application Services \(AS\), Supporting Offerings \(SO\), Business Processes \(BP\), and Dependencies modules in the map view.

You can configure node dependency directions and enhance visual elements with improved colors and icons for clarity. Additionally, you can gain comprehensive insights from the summary panel and address missing 'red flags' for a complete picture.

-   **[Generate Word reports of action tasks](https://www.servicenow.com/docs/access?context=gen-word-reports&family=zurich&ft:locale=en-US)**

Use the Document designer to set up Microsoft Word templates and download action task reports in Digital resilience incident reporting. This functionality enables you to customize predefined templates or create templates, incorporating specific data like tables and columns from records, to generate intuitive, audit-ready reports. You can then save these reports within the ServiceNow® instance or as cloud documents in Microsoft SharePoint.

-   **[Report incidents associated with multiple regulations for various legal entities](https://www.servicenow.com/docs/access?context=reporting-for-multiple-regulations&family=zurich&ft:locale=en-US)**

Report incidents or security incidents associated with multiple regulations for various legal entities in Digital resilience incident reporting. Its automated workflow generates regulatory reporting assessment of IT incidents, DRI Initial report, DRI Intermediate report, and DRI Final report within regulatory timelines, each with dedicated action tasks. You can complete these tasks and generate reports in Microsoft Word format required by regulatory authorities for analysis.

-   **[Generate Register of Information \(RoI\) regulatory packages](https://www.servicenow.com/docs/access?context=opres-dora-roi-reg-pkg&family=zurich&ft:locale=en-US)**

Generate regulator-ready Register of Information \(RoI\) regulatory packages using the Plain-CSV Report Package option on the download page in Digital resilience third-party registers. The resulting ZIP file, structured to regulator specifications, includes metadata and report folders with file names containing LEI, entity ID, and release version.

This format helps you to verify EU DORA compliance and supports automated validation workflows. For suggested steps and permissions, refer to the user guide on the Download and Upload request page.

-   **[Validate downloaded Register of Information regulatory packages](https://www.servicenow.com/docs/access?context=opres-dora-validate-roi&family=zurich&ft:locale=en-US)**

Validate downloaded Register of Information \(RoI\) regulatory packages against requirements using the Plain-CSV Report Package option on the Digital resilience third-party registers download page. This process verifies file format, structure, encoding, naming conventions, and field-level data across multiple tables.

If validation warnings are detected, an automated report is attached, mapping issues to regulator fields like Template Code, Row Code, and Column Code. These reports include real-world field labels, rule expressions, and record identifiers. You can easily cross-reference validation errors using a downloadable Excel template that mirrors the CSV structure, simplifying issue location and resolution. Further enhancements include support for 'Not applicable' values, enforced file size limits, and clearer error messages for malformed data.

-   **[Improve resilience metrics with the enhanced CSDM model](https://www.servicenow.com/docs/access?context=using-csdm-v5&family=zurich&ft:locale=en-US)**

Leverage the enhanced fix scripts in the Common Service Data Model \(CSDM\) to enhance your Operational Resilience metrics. Each node in the hierarchy is now stored separately, with its class and parent nodes, to help you manage your data more efficiently.

The **Update CSDM and other dependencies** scheduled job script has been optimized to process the main node configurations in parallel, triggering a separate event for each node. Any node can be at the top level. Additionally, you can store impacted objects, including all parents, in a single table, so that you can efficiently retrieve children nodes and improve your data retrieval.

Configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class. You can view the downstream data and various dashboards based on the selected top class, such as the number of application services that are under a business service.

-   **[Analyze importance and impact tolerance of a service using Smart Assessment](https://www.servicenow.com/docs/access?context=create-an-assessment-for-services-in-ws&family=zurich&ft:locale=en-US)**

Analyze a service's importance and impact tolerance through flexible assessments by using one or multiple Smart Assessment templates. Role-based access controls and auto-assigned tasks help you to streamline the process. You can reopen and complete assessments as needed and send email notifications to relevant users.

-   **[Generate customized and flexible self-attestation reports using Smart Assessment](https://www.servicenow.com/docs/access?context=create-new-attestation-in-ws&family=zurich&ft:locale=en-US)**

Generate customized and flexible self-attestation reports by using Smart Assessment. Start with the default template, add relevant scopes and users, and generate a PDF report on completion of the self-attestation process. By creating custom templates with various data types, you make the self-attestation process more efficient.

-   **[Leverage enhanced DORA capabilities for contracts, supply chains, and assessments](https://www.servicenow.com/docs/access?context=create-drtp-reg-contract&family=zurich&ft:locale=en-US)**

Use the enhanced Digital Operational Resilience Act \(DORA\) data model in Operational Resilience. You can configure contracts based on their supply chains and assessments, upload the contract records, and generate a detailed report in Microsoft Excel that provides information on the entities, third parties, and specific contract details.

-   **[Track third-party risk assessments](https://www.servicenow.com/docs/access?context=opres-ws-homepage-overview&family=zurich&ft:locale=en-US)**

Track third-party risk assessments as red flags in Operational Resilience reports and overview pages for business services, service offerings, and business processes. Operational Resilience users, managers, and administrators can review these assessments in Operational Resilience Workspace. The sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer role is now included in the sn\_oper\_res.user role, so that you can grant the necessary access to the assessments.


</td></tr><tr><td>

Australia

</td><td>

-   **[Export action task reports](https://www.servicenow.com/docs/access?context=work-on-action-tasks&family=australia&ft:locale=en-US)**

Export DRIR assessment action task reports in Microsoft Word, Microsoft Excel, or JSON format from a drop-down menu. Generate Microsoft Word documents for narrative reports, Microsoft Excel spreadsheets with structured question-answer layouts, or JSON files for system integrations.

-   **[Create Reporting configurations](https://www.servicenow.com/docs/access?context=create-reporting-configurations&family=australia&ft:locale=en-US)**

Manage document outputs centrally with the Reporting Configurations module in Digital resilience incident reporting. Administrators can manage template configurations, content configurations, and data relationship configurations from one place.

-   **[Convert and aggregate contractual expenses to regulator-required currencies](https://www.servicenow.com/docs/access?context=currency-conversion-aggregation&family=australia&ft:locale=en-US)**

Standardize annual expense values during Register of Information report generation by enabling optional currency conversion and third-party total expense aggregation. The application converts contract amounts to a base currency using 32 European Central Bank \(ECB\) exchange rates based on the reference date. Administrators upload monthly rates into the system. When eligibility criteria are met, expenses across multiple contracts are aggregated by third-party providers or engagements, generating consolidated reports that comply with DORA regulatory requirements.

-   **[Validate Legal Entity Identifiers using GLEIF API](https://www.servicenow.com/docs/access?context=create-legal-entity&family=australia&ft:locale=en-US)**

Validate Legal Entity Identifiers \(LEIs\) in real time against the GLEIF API across all four record form types — Legal Entity, Branch, Third Party, and Third Party Engagement. Name and country fields are auto-populated or cross-checked on create and update, with warnings shown on mismatch.

During Microsoft Excel upload, a batch verification consolidates and validates all LEIs against GLEIF before processing, flagging warnings while allowing administrators to save flagged rows for later correction. During CSV package download, a dedicated LEI validation report is generated.

-   **[GLEIF API performance using system properties](https://www.servicenow.com/docs/access?context=properties-dora&family=australia&ft:locale=en-US)**

Configure GLEIF API behavior using the following system properties:

    -   **sn\_dora\_accel.gleif\_api\_batch\_size** — Controls how many LEIs are sent per request.
    -   **sn\_dora\_accel.gleif\_api\_timeout\_ms** — Sets the HTTP timeout per API call.
    -   **sn\_dora\_accel.lei\_save\_on\_gleif\_error** — Controls whether rows that fail GLEIF validation during Microsoft Excel upload are saved with warnings or rejected.
-   **[Monetary values for DORA reporting](https://www.servicenow.com/docs/access?context=properties-dora&family=australia&ft:locale=en-US)**

Control monetary value precision in DORA reports using the **sn\_dora\_accel.decimals\_monetary** system property. Set it to 0 to round to whole units, or a negative value \(for example, -3\) to round to thousands, based on regulator requirements.

-   **Duplicate record detection and warnings in DORA reporting [Create Microsoft Excel download and upload request](https://www.servicenow.com/docs/access?context=create-excel-upload-download-request&family=australia&ft:locale=en-US)**

Detect and prevent duplicate DORA records across key workflows. A business rule blocks saving on the Contractual Arrangement form when a duplicate record is detected. Warnings are displayed when duplicate rows are found during CSV downloads.

-   **[Run advanced scenario analysis using simulation](https://www.servicenow.com/docs/access?context=scenario-analysis-playbook-experience&family=australia&ft:locale=en-US)**

Plan and run advanced scenario analysis on a dedicated Scenario Analysis record, capturing simulation method, dependencies, and assignee. Progress through a guided Playbook with stages for dependency scoping, scenario testing, result review, impact assessment, and final completion.

Execute statistical model profiles to evaluate severe-but-plausible scenarios across services and dependencies. The record is locked once the treatment decision and reason are recorded.

-   **[Template versions](https://www.servicenow.com/docs/access?context=set-up-sae-templates&family=australia&ft:locale=en-US)**

Track Smart Assessment Engine \(SAE\) template versions across assessment flows. New assessments automatically use the latest published Smart Assessment template version, while existing records on older versions continue to function without disruption. Assessment questions and automation logic handle different template versions correctly within the same flow.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Operational Resilience features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For more information, see

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Operational Resilience features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Operational Resilience features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The Operational Resilience application previously stored the entire dependency chain in the \[sn\_oper\_res\_profile\] table, which resulted in redundant data and potential performance issues. The **Update CSDM and other dependencies** scheduled job script has been optimized to address this issue. Any node can now be at the top level. Data retrieval is more efficient because you can store the impacted objects in a single table.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Operational Resilience.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Operational Resilience by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Operational Resilience by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Resilience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Operational Resilience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

</td></tr><tr><td>

Zurich

</td><td>

Operational Resilience requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Operational Resilience, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Operational Resilience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Operational Resilience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Align with the CSDM model to set up configurable main node configurations, which are used to retrieve CSDM and their dependency data.
-   Add the primary origin to an operational vulnerability, and the impacted areas are automatically included. The vulnerability can then be viewed from any impacted area.
-   All CSDM objects, dependencies, and their red flags can be rolled up based on the entity hierarchy.
-   Use Smart Assessment for evaluating an Operational vulnerability.

 See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Set up the nexus map configurations and use the interactive node map view to define dependencies and relationships between records.
-   Generate a Microsoft Word document for the action tasks in Digital resilience incident reporting.
-   Create DIR cases for multiple regulations from either an incident or a security incident report. You can map entities to regulations and configure the Smart Assessment Engine \(SAE\) template for each regulation within the regulatory agency profile.
-   Generate and validate regulator-ready Register of Information \(RoI\) packages for EU DORA compliance.
-   Use the enhanced fix scripts in the Common Service Data Model for improved Operational Resilience metrics.
-   Evaluate the importance and impact tolerance of services and self-attest their status by using Smart Assessment.

 See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Export Digital resilience incident reporting \(DRIR\) action tasks in Microsoft Word, Microsoft Excel, or JSON for regulatory reporting.
-   Run an advanced scenario analysis with guided steps for dependency mapping, statistical modeling, scenario testing, and impact review.
-   Generate consistent, regulator-ready reports using optional currency conversion and third-party expense aggregation in Digital Operational Resilience Act \(DORA\) Register of Information reporting.
-   Validate Legal Entity Identifiers \(LEIs\) in real time against the Global Legal Entity Identifier Foundation \(GLEIF\) API across record forms, CSV downloads, and Microsoft Excel uploads. Use the LEI Validation Report for compliance tracking.
-   Customize DRIR document outputs through Reporting and Template configuration modules.

 See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

