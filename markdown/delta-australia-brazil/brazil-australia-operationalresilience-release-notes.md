---
title: Combined Operational Resilience release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Operational Resilience from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-operationalresilience-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Operational Resilience release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Operational Resilience from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Resilience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Resilience to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

