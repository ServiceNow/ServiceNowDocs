---
title: Combined Operational Resilience release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Operational Resilience from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-operationalresilience-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Operational Resilience release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Operational Resilience from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Resilience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Resilience to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[Managing Operational vulnerability](https://www.servicenow.com/docs/access?context=operational-vulnerability&family=xanadu&ft:locale=en-US)**

Address operational vulnerabilities through reporting, assessing impact, evaluating criticality, managing issues, and planning treatments in Operational Resilience Workspace. Report operational vulnerabilities by using either Employee Center or Operational Resilience Workspace.

-   **[Maintaining Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=digi-resi-third-party-registers&family=xanadu&ft:locale=en-US)**

Comply with Digital Operational Resilience Act \(DORA\) regulation requirements by creating contractual arrangements between the financial entities and the ICT service providers in Digital resilience third-party registers. The ICT third-party service provider records are maintained in Digital resilience third-party registers for DORA compliance.

Add or modify the records in bulk or individually for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements. Export the records to Microsoft Excel format for the European Union to streamline the auditing process as per the regulation. You have the option to import the records from external sources into the Digital resilience third-party registers application.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Using Digital resilience incident reporting](https://www.servicenow.com/docs/access?context=drir-module&family=yokohama&ft:locale=en-US)**

Assess whether any critical services are affected and classify the reported incident as a major incident if necessary. Notify regulators of major incidents, categorized by their severity and security ratings.

The Digital resilience incident reporting module, accessible from the Operational Resilience Workspace, is integrated with Incident Management and Security Incident Response to generate and share reports in the format that is specified by the regulators.

You can generate an initial report within 24 hours, an intermediate report within 72 hours, and a final report within 1 month. All of these reports are automatically triggered by the application from the time that the incident is classified as a major incident.


</td></tr><tr><td>

Zurich

</td><td>

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

Xanadu

</td><td>

-   **[Reporting Operational vulnerability](https://www.servicenow.com/docs/access?context=reporting-operational-vul&family=xanadu&ft:locale=en-US)**

The Operational vulnerability related list has been added to the following modules in the List view:

    -   Importance and impact tolerance assessment
    -   Scenario analyses
    -   Self attestations
    -   Services

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Addition of classes to the assessment form](https://www.servicenow.com/docs/access?context=submit-an-assessment-in-ws&family=yokohama&ft:locale=en-US)**

The Business Service and Offering classes have been added to the **Scope** tab of the assessment form, enabling you to assess the business services and service offerings alongside services. Once the assessment is complete, the importance and impact tolerance of these items are displayed in the Importance and Impact Tolerance columns on the **Scope** tab.

-   **[Addition of classes to the scenario analysis form](https://www.servicenow.com/docs/access?context=scenario-analysis-in-ws&family=yokohama&ft:locale=en-US)**

The Business Service and Offering classes have been added to the **Scope** tab of the scenario analysis form, enabling you to analyze the business services and service offerings alongside services.

-   **[Addition of classes to the self-attestation form](https://www.servicenow.com/docs/access?context=self-attestation-in-ws&family=yokohama&ft:locale=en-US)**

The Business Service and Offering classes have been added to the **Scope** tab of the self-attestation form, enabling you to self-attest the business services and service offerings alongside services.

-   **[Digital resilience incident reporting module](https://www.servicenow.com/docs/access?context=drir-module&family=yokohama&ft:locale=en-US)**

The Digital resilience incident reporting module is used to report the Information and Communication Technology \(ICT\) related incidents to the regulators.


</td></tr><tr><td>

Zurich

</td><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

</td></tr><tr><td>

Yokohama

</td><td>

-   **Browser requirements**

Business Continuity Management requires the following browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

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

Xanadu

</td><td>

Improved screen reader and translation support by adding ARIA button labels, tooltips, and alt text to the Operational Resilience Workspace. This support provides an explanation for button actions and identifies tooltip text to be translated.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   Monitor business service resiliency from start to finish, with a focus on operational risk and compliance.
-   Identify and report operational vulnerabilities from Employee Center or Operational Resilience Workspace. Address these vulnerabilities through procedures such as reporting, assessing impact, evaluating criticality, managing issues, and planning treatments.
-   Use the Digital resilience third-party registers application to establish, update, and manage contractual arrangements between the financial entities and Information and Communication Technology \(ICT\) service providers.
-   Export the records for regulators and auditors in Microsoft Excel format by using the Microsoft Excel upload capability in Digital resilience third-party registers. Similarly, you can import the records from external sources by using the Microsoft Excel download functionality.

 See [Managing Operational vulnerability](https://www.servicenow.com/docs/access?context=operational-vulnerability&family=xanadu&ft:locale=en-US) and [Maintaining Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=digi-resi-third-party-registers&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

-   Identify, assess, and monitor operational risks across people, processes, systems, and external dependencies to understand impact on critical business services and customer outcomes.
-   Develop and execute resilience strategies, conduct scenario testing, and track remediation actions to strengthen your organization's ability to withstand and recover from operational disruptions.

 See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

