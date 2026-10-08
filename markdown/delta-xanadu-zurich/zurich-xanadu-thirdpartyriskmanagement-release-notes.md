---
title: Combined Third-party Risk Management release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Third-party Risk Management from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-thirdpartyriskmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 22
breadcrumb: [Products combined by family]
---

# Combined Third-party Risk Management release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Third-party Risk Management from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Third-party Risk Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Third-party Risk Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Upgrade information**

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=yokohama&ft:locale=en-US).

For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.


</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=zurich&ft:locale=en-US).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings.


</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Third-party element collection](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&family=xanadu&ft:locale=en-US)**

Confirm that third-party elements adhere to the same security and compliance standards as an engagement by monitoring them through TPRM. Use this data to help identify, assess, and manage the risks that are related to your engagements that depend on third-party elements.

-   **[Risk intelligence report requests](https://www.servicenow.com/docs/access?context=tprm-riskintel-using&family=xanadu&ft:locale=en-US)**

Make informed decisions about working with an engagement or third party by requesting and managing risk intelligence reports or scores from external risk intelligence content providers using the Third-party Risk Management application.

-   **[Third-party risk management data model](https://www.servicenow.com/docs/access?context=tprm-data-model&family=xanadu&ft:locale=en-US)**

Take full advantage of Third-party Risk Management by viewing its data model to see how you can best use it to assess, monitor, and mitigate the risks that are required for your risk management program.

-   **[Digital resilience third-party registers](https://www.servicenow.com/docs/access?context=tprm-dora&family=xanadu&ft:locale=en-US)**

Create, update, and track records for digital resilience third-party registers by using the Digital resilience third-party registers application within the Vendor Management Workspace Vendor Management Workspace. You can bulk create or edit individual records for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements using the Excel download/upload requests feature. This application helps you maintain records with information and communication technology \(ICT\) third-party service providers, helping ensure compliance with the Digital Operational Resilience Act \(DORA\).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[New Standardized Information Gathering \(SIG\) questionnaire content](https://www.servicenow.com/docs/access?context=grc-sig-integration&family=yokohama&ft:locale=en-US)**

Use the updated SIG templates for 2025 after upgrading to version 20.1.x as part of the Third-party Risk Management application. The latest SIG questionnaires help your organization stay aligned with stricter regulatory compliance and emerging third-party risk governance, covering a wide range of security and privacy concerns.


 -   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&family=yokohama&ft:locale=en-US)**

Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=yokohama&ft:locale=en-US)**

Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US)**

Review the ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes for full descriptions of the features.

-   **[Use the Document Management System](https://www.servicenow.com/docs/access?context=tprm-dms&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

For information on Now Assist skills for TPRM and Document Management, see [ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US) and [Now Assist in Document Intelligence release notes](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-rn&family=zurich&ft:locale=en-US).

-   **[Register of information regulatory packages](https://www.servicenow.com/docs/access?context=tprm-dora-roi&family=zurich&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can now generate regulator-ready Register of Information packages using the Plain-CSV Report Package option on the download page. The ZIP file includes metadata and report folders structured to regulator specifications, with file names containing LEI, entity ID, and release version. This format helps ensure EU DORA compliance and supports automated validation workflows. You can follow the user guide on the Download/Upload request page for suggested steps and permissions.

-   **[Validation framework for RoI](https://www.servicenow.com/docs/access?context=tprm-validation-roi&family=zurich&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can now validate downloaded Register of Information packages using the Plain-CSV Report Package option on the download page against requirements. File format, structure, encoding, naming conventions, and field-level data are validated across multiple tables. If any validation warnings are detected, a validation report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. Validation reports include real-world field labels, rule expressions, and record identifiers. You can cross-reference validation errors using a downloadable Excel master template that mirrors the CSV structure, making it easier to locate and address issues. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data.


 -   **[New sn\_vdr\_risk\_asmt.sae\_enabled property](https://www.servicenow.com/docs/access?context=tprm-properties-configure&family=zurich&ft:locale=en-US)**

Use the new and improved Smart Assessment experience after you upgrade to version 21.0.x and set the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Smart Assessment Engine](https://www.servicenow.com/docs/access?context=tprm-sae-using&family=zurich&ft:locale=en-US)**

Create Smart Assessment Engine assessments for your organization:

    -   Enhanced navigation: Use the improved navigation for a better user experience.
    -   Assessment support: Conduct assessments for both internal and external parties. TPRM questionnaire templates include additional attributes such as the risk area and the option to include previous responses, which aren’t available in SAE. TPRM templates must be created directly within the Vendor Management Workspace to ensure that they include the necessary attributes.
    -   Organize questions: Group questions into subsections for better organization.
    -   Add attachments: Attach the files directly to the individual questions.
    -   Add reference information: Add reference information to a questionnaire template to help ensure that assessors can access the information they need while responding.
    -   Filter questions: Quickly identify and filter unanswered questions.
    -   Auto-save for questionnaires: Auto-save each question automatically after changes are made to them.
    -   Standardized risk rating scale definition: Define the risk rating scales at the template level for both internal and external assessments.
    -   Assessment duration: Define the duration of an assessment when creating a questionnaire template.
    -   Combine assessments: Respond to questionnaires by using the same SAE template in a single, streamlined view.
    -   Bulk template migration: Migrate classic templates in bulk to the Smart Assessment format. To ensure the templates work correctly in TPRM, you must migrate them by using the Third-party Risk Management application.
    -   Risk score normalization: Standardize the risk scores for a consistent evaluation.
    -   Support for the GRC and third-party portals: Use the GRC portal to access and complete internal assessments and the third-party portal to complete external assessments.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Third-party Risk Management features.

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

-   **[Multiple legal entities making use of the services for contracts](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], add multiple legal entities that are using services as part of a contract record in the digital resilience third-party registers within the Vendor Management Workspace. Including all entities that are using services associated with a contract is essential for maintaining transparency, helping ensure compliance, and enhancing operational resilience.


 -   **[Codes and additional identification information for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-ICT-thirdparty-serv-prov-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **[Function types for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-new-function-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.


 -   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&family=yokohama&ft:locale=en-US)**

The Third-party insights dashboard and the TPRM custom analytics dashboard are now available from the Dashboards page of the Vendor Management Workspace.

-   **[Third-party portal import modal](https://www.servicenow.com/docs/access?context=tprm-excel-template-support&family=yokohama&ft:locale=en-US)**

The import modal now enables you to respond to questionnaires by using a Microsoft Excel template. You can download the questionnaire, complete it according to the included instructions, and import the final version into the Third-party portal.


 -   **[Pre-populate responses using questionnaires](https://www.servicenow.com/docs/access?context=tprm-assessing-tpr&family=yokohama&ft:locale=en-US)**

If you have the Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can enable third-party and engagement contacts to review and update responses only if necessary by pre-populating questionnaires for engagements and entities with responses from completed questionnaires that are associated with the same third party. The attachment, duration, and signature type responses are excluded. This feature also helps ensure data consistency and accuracy.

-   **[Microsoft Excel questionnaire template](https://www.servicenow.com/docs/access?context=tprm-excel-template-support&family=yokohama&ft:locale=en-US)**

Streamline the due diligence process by enabling third-party and engagement contacts to respond to questionnaires using a Microsoft Excel template by downloading the questionnaire as a template, completing it according to the included instructions, and importing the final version into the Third-party portal. This feature update enhances flexibility by enabling third-party and engagement contacts to provide information outside the third-party portal. Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access this feature and respond to questionnaires on behalf of Third-party and engagement contacts through the Vendor Management Workspace.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Vertical navigation in the Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-monitoring-tpr&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, the legacy horizontal tab-based layout in the Vendor Management Workspace has been replaced with a structured vertical navigation panel with groups of related lists, organizing access to third-party records, assessments, and performance pages in a way that supports clearer workflows and is consistently available to all internal users.

-   **[Third-party information register download option renamed to Excel master template](https://www.servicenow.com/docs/access?context=tprm-excel-upload-download-request&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, the option to download the Third-party Information Register is renamed to Excel Master Template. This change improves clarity and aligns with regulator terminology.

-   **[DPM business validation rules and properties](https://www.servicenow.com/docs/access?context=tprm-validation-roi&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, the DPM business validation rules and report.json, reportPackage.json, FrameworkCodeModuleVersion properties are now included. These modules enable Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] to view and maintain validation logic and configuration settings for CSV reporting and automated validation.

-   **[Choice field for ICT third-party service provider identification](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, the field **Type of code to identify the ICT third-party service provider** is now updated to be a choice field in the Digital Resilience Third-party Information Register in the contract record. This update aligns the field with regulator-defined options for selecting identification systems when creating new providers. In the Specific Information section of the contract record, the field is read-only and auto-populated based on upstream selections, such as the third-party or engagement record.


 -   **[Risk areas extended to internal assessments](https://www.servicenow.com/docs/access?context=create-sae-q-template&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, if you have the third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_admin\] role, you can now configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace. Risk scores can be aggregated at the engagement level using customizable methods such as max, min, or average, and mapped to risk ratings based on business rules. Risk managers can override system-generated ratings with required justification, enabling expert judgment and helping ensure transparency in risk decisions.

-   **[Smart Assessment Engine advanced plugins](https://www.servicenow.com/docs/access?context=tprm-migrate-asmnt-sae&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, the following Smart Assessment Engine advanced plugins are automatically installed: Post Assessment Actions for Smart Assessments \[com.sn\_smart\_imp\_auto and com.sn\_impact\_fwk\] and Advanced Response Automation for Smart assessments \[sn\_smart\_resp\_auto\]. The Post Assessment Actions for Smart Assessments plugin lets Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] automate follow-up tasks, like notifications or workflow launches, after an assessment is completed. The Advanced Response Automation for Smart Assessments plugin automatically fills in assessment responses based on prior data or logic, streamlining and standardizing the assessment process.

-   **Feature-specific administrator role enhancements**

Starting with version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

    -   Assign sn\_vdr\_risk\_asmt.vendor\_risk\_admin to users who need to configure and manage vendor risk features.
    -   Assign sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer to users who perform assessments, manage dashboards, and require operational access.
    -   Assign sn\_vdr\_risk\_asmt.external\_assessment\_responder to users who need access to the third-party portal and to complete assessments.

**Note:** Administrator privileges no longer grant access to TPRM features. Users must be assigned an appropriate feature-specific role to access relevant functionality.

-   **Read-only field enhancements**

Starting with version 21.1.x, the following Third-party Risk Management plugins have security enhancements for read-only fields in this release:

    -   Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\]
    -   Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\]
    -   GRC: Vendor Portal \[com.sn\_grc\_vendor\_portal\]
    -   GRC: Profiles \[com.sn\_grc\]
    -   GRC: Compliance Assessment \[com.sn\_comp\_asmt\]
    -   GRC: SIG Questionnaire Integration \[com.sn\_sig\_asmt\]
    -   GRC: Performance Analytics Premium Integration \[com.sn\_grc\_pa\]
    -   Vendor Risk Management integration with EcoVadis \[com.sn\_app\_grc\_ecovadis\]
    -   ITAM applications \[com.snc.vendor\_core\]
-   **[Fourth-party assessment support in SAE](https://www.servicenow.com/docs/access?context=tprm-monitor-fourth-parties&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, Fourth-party assessments are now supported after you enable the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.


 -   **Global TPRM changes**
    -   Assessments and Third-party assessments are now renamed as External assessments.
    -   Tiering assessments are now renamed as Internal assessments.
    -   The Tier-level column is now renamed as Risk rating.
    -   The Tiering assessors column is now renamed as Respondents.
    -   The **Owner** field is now renamed as **Assigned to** on the internal assessment, external assessment, tiering assessment, and due diligence request forms.
-   **[Changes made to the list view in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-ws-list-page&family=zurich&ft:locale=en-US)**
    -   The Assessment setup section has been added. From this section, you can create assessment templates, Smart Assessment questionnaire templates, and issue generation rules.
    -   The Questionnaire requests section has been added.
    -   The Tiering assessments and Inherent risk questionnaires \(IRQ\) are combined in the Internal assessments section.
-   **Changes made to internal assessment pages**
    -   Tier-level scales are renamed as Scales.
    -   Tiering assessment schedule and Schedules are combined and renamed as Assessment schedule.
-   **Changes made to assessment related lists**
    -   Assessment instances is renamed as Questionnaire requests.
    -   Questionnaires is renamed as Questionnaire templates.
    -   Document requests is renamed as Document templates.
    -   Fourth-party questionnaires is renamed as Fourth-party templates.
    -   Repeating assessments is renamed as Assessment scheduling.
-   **[Smart Assessment integration changes](https://www.servicenow.com/docs/access?context=tprm-sae-using&family=zurich&ft:locale=en-US)**
    -   The Assessment engine column has been added to the Internal and External assessment list views in Vendor Management Workspace. You can track the assessment type as you transition to using the Smart Assessment Engine for all active questionnaires.
    -   The **Assessment engine** field has been added to related forms for internal risk assessments, external risk assessments, and assessment templates.
    -   The Support smart assessment column has been added to the Assessment templates and Issue generation rules list views.
    -   The original TPRM **Classification** field has been replaced with the **Purpose** field on all assessment templates.
    -   The external assessment status **Responses received** is now **Submitted to third party** when SAE is enabled.
    -   The external assessment status **Returned** is now **In progress** when SAE is enabled.
-   **[Changes made to Digital Resilience Third-party Information Register contract records in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=zurich&ft:locale=en-US)**

The General info related list has now been renamed as Details and the following related lists have been added:

    -   Entities signing contract to use service
    -   Entities making use of services
    -   Entities providing services
    -   Third parties signing contract to provide services
    -   Third-party engagements signing contract
    -   ICT service supply chains
    -   Assessments of the ICT services
-   **Coral theme**

Coral is now the default theme for Vendor Management Workspace, portal, and mobile experiences. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

**Note:** When you're upgrading from Xanadu or Yokohama to Zurich with version 20.1.x of the GRC: Vendor Portal, the application UI themes might not match. The Vendor Management Workspace uses the Polaris theme by default, and the Third-party portal uses the Coral theme by default. Upgrading to Xanadu or Yokohama with version 20.1.x of the GRC: Vendor Portal results in both the Vendor Management Workspace and Third-party portal using the Polaris theme. Upgrading to version 21.x or higher results in both the Vendor Management Workspace and Third-party portal using the Coral UI theme.


 -   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=zurich&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Third-party Risk Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Third-party Risk Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Reminder workflows](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&family=xanadu&ft:locale=en-US)**

Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won’t be deprecated or migrated as part of this change.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

 [Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=xanadu&ft:locale=en-US). After upgrades and deployments of new applications or integrations, run quick start tests to verify that TPRM works as expected. If you customized TPRM, copy the quick start tests and configure them for your customizations.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Third-party Risk Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Accessibility improvements for the Third-party Risk Management application include the following updates.

-   Keyboard focus: Improved visual accessibility in the Third-party portal by increasing contrast between the focus border and white background.
-   Screen reader support has been extended to announce the following:
    -   Completed status after all questions have been completed in a section of an external questionnaire in the Third-party portal.
    -   Correct labels and other relevant information for controls, images, card regions, menu items, and links in the Vendor Management Workspace.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for the Vendor Management Workspace and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Third-party Risk Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Collect, monitor, and assess third-party elements for engagements.
-   Request risk intelligence reports \(RIR\) and scores so that you can manage and monitor your RIR requests all within TPRM.
-   View the Third-party Risk Management data model.
-   Use the Digital resilience third-party registers application to create, update, and track records for digital resilience third-party registers.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Pre-populate questionnaires for entities and engagements that are associated with the same active third party by using responses from complete questionnaires.
-   Respond to questionnaires by using a Microsoft Excel questionnaire template.
-   Explore and analyze assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard.
-   Stay aligned with stricter regulatory compliance and emerging third-party risk governance by using the new Standardized Information Gathering \(SIG\) questionnaire content available for 2025.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use the Document Management system in TPRM to centralize third-party documentation in a searchable repository with metadata, and versioning, access controls.
-   Use vertical navigation in the Vendor Management Workspace through a customizable panel grouped by related lists for improved access to third-party records, assessments, and performance pages.
-   Configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace.
-   Use the latest Smart Assessment Engine questionnaire templates to perform internal and external assessments.
-   Use the enhanced Digital Resilience Third-party Information Register features in the Vendor Management Workspace.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

