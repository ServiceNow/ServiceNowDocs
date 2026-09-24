---
title: Combined Operational Resilience release notes for upgrades from Zurich to Brazil
description: Consolidated page of all release notes for Operational Resilience from Zurich to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-brazil/brazil-zurich-operationalresilience-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Operational Resilience release notes for upgrades from Zurich to Brazil

Consolidated page of all release notes for Operational Resilience from Zurich to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Resilience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Resilience to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Upgrade information**

After upgrading to Operational Resilience version 21.0.x, rerun the **Update CSDM and other dependencies** scheduled job to populate the additional metadata that was introduced in this release.


</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

Beginning with Operational Resilience release 22.0.x, the following scheduled jobs are deactivated for new installations by default:

    -   **Calculate red flags for CSDM and dependencies**
    -   **Update CSDM and other dependencies**
For existing installations, these jobs retain their current active or inactive state.


</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Operational Resilience.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **[Create Reporting configurations](https://www.servicenow.com/docs/access?context=create-reporting-configurations&family=australia&ft:locale=en-US)**

Manage document outputs centrally with the Reporting Configurations module in Digital resilience incident reporting. Administrators can manage template configurations, content configurations, and data relationship configurations from one place.

-   **[Validate Legal Entity Identifiers using GLEIF API](https://www.servicenow.com/docs/access?context=create-legal-entity&family=australia&ft:locale=en-US)**

Validate Legal Entity Identifiers \(LEIs\) in real time against the GLEIF API across all four record form types — Legal Entity, Branch, Third Party, and Third Party Engagement. Name and country fields are auto-populated or cross-checked on create and update, with warnings shown on mismatch.During Microsoft Excel upload, a batch verification consolidates and validates all LEIs against GLEIF before processing, flagging warnings while allowing administrators to save flagged rows for later correction. During CSV package download, a dedicated LEI validation report is generated.

-   **[GLEIF API performance using system properties](https://www.servicenow.com/docs/access?context=properties-dora&family=australia&ft:locale=en-US)**

Configure GLEIF API behavior using the following system properties:

    -   **sn\_dora\_accel.gleif\_api\_batch\_size** — Controls how many LEIs are sent per request.
    -   **sn\_dora\_accel.gleif\_api\_timeout\_ms** — Sets the HTTP timeout per API call.
    -   **sn\_dora\_accel.lei\_save\_on\_gleif\_error** — Controls whether rows that fail GLEIF validation during Microsoft Excel upload are saved with warnings or rejected.
-   **[Duplicate record detection and warnings in reporting](https://www.servicenow.com/docs/access?context=create-excel-upload-download-request&family=australia&ft:locale=en-US)**

Detect and prevent duplicate DORA records across key workflows. A business rule blocks saving on the Contractual arrangement form when a duplicate record is detected. Warnings are displayed when duplicate rows are found during CSV downloads.

-   **[Run advanced scenario analysis using simulation](https://www.servicenow.com/docs/access?context=scenario-analysis-playbook-experience&family=australia&ft:locale=en-US)**

Plan and run advanced scenario analysis on a dedicated Scenario analysis record, capturing simulation method, dependencies, and assignee. Progress through the guided **Playbook** with stages for dependency scoping, scenario testing, result review, impact assessment, and final completion.Execute statistical model profiles to evaluate severe-but-plausible scenarios across services and dependencies. The record is locked once the treatment decision and reason are recorded.

-   **[Template versions](https://www.servicenow.com/docs/access?context=set-up-sae-templates&family=australia&ft:locale=en-US)**

Track Smart Assessment Engine \(SAE\) template versions across assessment flows. New assessments automatically use the latest published Smart Assessment template version, while existing records on older versions continue to function without disruption. Assessment questions and automation logic handle different template versions correctly within the same flow.


 -   **[Export action task reports](https://www.servicenow.com/docs/access?context=work-on-action-tasks&family=australia&ft:locale=en-US)**

Export DRIR assessment action task reports in Microsoft Word, Microsoft Excel, or JSON format from a drop-down menu. Generate Microsoft Word documents for narrative reports, Microsoft Excel spreadsheets with structured question-answer layouts, or JSON files for system integrations.

-   **[Convert and aggregate contractual expenses to regulator-required currencies](https://www.servicenow.com/docs/access?context=currency-conversion-aggregation&family=australia&ft:locale=en-US)**

Standardize annual expense values during Register of Information report generation by enabling optional currency conversion and third-party total expense aggregation. The application converts contract amounts to a base currency using 32 European Central Bank \(ECB\) exchange rates based on the reference date. Administrators upload monthly rates into the system. When eligibility criteria are met, expenses across multiple contracts are aggregated by third-party providers or engagements, generating consolidated reports that comply with DORA regulatory requirements.

-   **[Monetary values for DORA reporting](https://www.servicenow.com/docs/access?context=properties-dora&family=australia&ft:locale=en-US)**

Control monetary value precision in DORA reports using the **sn\_dora\_accel.decimals\_monetary** system property. Set it to 0 to round to whole units, or a negative value \(for example, -3\) to round to thousands, based on regulator requirements.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Operational Resilience features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Main node configurations: A component of the Data Relationship Framework](https://www.servicenow.com/docs/access?context=main-node-relationship-fw&family=zurich&ft:locale=en-US)**

The properties, related lists, and copy functionality in the Main node configurations form are updated.

-   **[Configure the Nexus map configurations](https://www.servicenow.com/docs/access?context=configure-nexus-map-configurations&family=zurich&ft:locale=en-US)**

The Nexus map configuration settings are added.

-   **[Node configurations and Node status configurations](https://www.servicenow.com/docs/access?context=configure-node-configurations&family=zurich&ft:locale=en-US)**

The Node configurations and Node status configurations related lists are added.

-   **[Edge configurations and edge status configurations](https://www.servicenow.com/docs/access?context=configure-edge-configurations&family=zurich&ft:locale=en-US)**

The Edge configurations and Edge status configurations related lists are added.

-   **[Interacting with the Nexus map UI from the Workspace](https://www.servicenow.com/docs/access?context=interacting-with-nexus-map-ui-from-worksapce&family=zurich&ft:locale=en-US)**

The **Resilience map** UI action is added to display the map view for a service record.

-   **[Word reports](https://www.servicenow.com/docs/access?context=reporting-for-multiple-regulations&family=zurich&ft:locale=en-US)**

The 'Template Configurations' module displays the document design template configuration details of DIR action tasks. The 'Word Templates' module provides the DIR Word templates used to generate Microsoft Word reports.

-   **[Regulation mappings related list](https://www.servicenow.com/docs/access?context=workflow-confi-auto-trigger-inci-repo-cases&family=zurich&ft:locale=en-US)**

The 'Digital Resilience Incident Case Type' module displays the ‘Digital Resilience Incident Case.’ The Regulation Mappings related list in the record shows the relationships between entities and their corresponding regulations.

-   **[Download the Excel template](https://www.servicenow.com/docs/access?context=create-excel-upload-download-request&family=zurich&ft:locale=en-US)**

The option to download the Third-party Information Register is renamed to Excel Master Template.


 -   **[Action tasks configuration related list](https://www.servicenow.com/docs/access?context=work-on-action-tasks&family=zurich&ft:locale=en-US)**

Action tasks configuration related list is used to set up contextual information for different regulations. This includes the assessment template, assignment group, trigger conditions, due dates, and more.

-   **[New modules and layout for Services](https://www.servicenow.com/docs/access?context=using-csdm-v5&family=zurich&ft:locale=en-US)**

The Application services module is added to the list view, which enables you to configure application services.A vertical layout is added for the Services, Business services, Offerings, Business processes, and Application services modules.In the CSDM objects table, the Impacted objects column displays the parent objects, while the Impacted objects classes column shows the classes. The Red flags count column indicates the number of the red flags that are directly assigned to a node, and the Total red flags count column displays the total count of the red flags directly assigned to a node and its children.

-   **[Contracts and related tabs for DORA](https://www.servicenow.com/docs/access?context=create-drtp-reg-contract&family=zurich&ft:locale=en-US)**

The related tabs for the contracts, including associated entities and third parties, are now shown in the Contract record forms.

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create Reporting configurations](https://www.servicenow.com/docs/access?context=create-reporting-configurations&family=australia&ft:locale=en-US)**

The Reporting Configurations module is provided in the Digital resilience incident reporting application to drive incident report generation.

-   **[Advanced scenario analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-playbook-experience&family=australia&ft:locale=en-US)**

The **Playbook** tab is provided in the Scenario analysis records.The **Statistical Modelling** and **Manual** options are available in the **Method** field on the **Details** tab.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Export action](https://www.servicenow.com/docs/access?context=work-on-action-tasks&family=australia&ft:locale=en-US)**

The **Export** UI action on the action task form displays the following options: **Generate MS Word**, **Export Excel**, and **Export JSON**.

-   **[Excel download/upload request form](https://www.servicenow.com/docs/access?context=create-excel-report-aggregate-expenses&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.0.x, the Excel download/upload request form includes the following fields for converting and aggregating contractual expenses to currencies required by regulators:

    -   **Report type**
    -   **Enable currency conversion**
    -   **Base currency**
    -   **Enable third-party total expense aggregation**
    -   **Reference date**
    -   **Date of the reporting**
The **Type** field includes the **Plain-csv reporting package** option for generating reports in Comma-Separated Values \(CSV\) format.A business rule checks eight composite key fields when saving a contractual arrangement and displays a warning if a duplicate is found. B.05\_02 includes a link to open the duplicate record directly for comparison. B.05\_01 correctly includes ICT Intra-Group Service Provider \(Legal Entity providers\) in the ICT Third-Party Service Provider report.A warning is displayed when a Legal Entity Identifier \(LEI\) fails validation or a mismatch is detected against the GLEIF API across all four record form types.

-   **[Template versions](https://www.servicenow.com/docs/access?context=set-up-sae-templates&family=australia&ft:locale=en-US)**

New assessments display the latest published Smart Assessment template version.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Operational Resilience features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Operational Resilience features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

The Operational Resilience application previously stored the entire dependency chain in the \[sn\_oper\_res\_profile\] table, which resulted in redundant data and potential performance issues. The **Update CSDM and other dependencies** scheduled job script has been optimized to address this issue. Any node can now be at the top level. Data retrieval is more efficient because you can store the impacted objects in a single table.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Operational Resilience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Australia is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Resilience we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Browser requirements**

Operational Resilience requires the following browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

-   Identify, assess, and monitor operational risks across people, processes, systems, and external dependencies to understand impact on critical business services and customer outcomes.
-   Develop and execute resilience strategies, conduct scenario testing, and track remediation actions to strengthen your organization's ability to withstand and recover from operational disruptions.

 See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-zurich-brazil/rn-combined-intro.md)

