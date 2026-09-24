---
title: Combined Third-party Risk Management release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Third-party Risk Management from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-thirdpartyriskmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 27
breadcrumb: [Products combined by family]
---

# Combined Third-party Risk Management release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Third-party Risk Management from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Third-party Risk Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Third-party Risk Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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


</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

If you're a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don't run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) is set to the default assessment engine and replaces the legacy experience. The transition is irreversible.

**Warning:** Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so can result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=australia&ft:locale=en-US).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content. Update any customizations that reference the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

After upgrading to version 22.3.3, the `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles. During upgrade, most users are automatically migrated to new feature‑specific roles. Users with custom role combinations may not be migrated automatically and require manual review before the grace period ends.


</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.

Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property makes the Smart Assessment Engine \(SAE\) the default assessment engine and replaces the legacy experience.

**Warning:** Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property is irreversible. Set this property in a non-production instance and test thoroughly before enabling it in production.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Third-party Risk Management.

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

-   **[TPRM personalized dashboards](https://www.servicenow.com/docs/access?context=tprm-monitor-dashboards&family=yokohama&ft:locale=en-US)**

Improve your decision-making process by exploring and analyzing your assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard. If you have the Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. If you're a third-party risk manager, you can also customize the report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs.

-   **[Quick start tests for TPRM](https://www.servicenow.com/docs/access?context=quick-start-tests-grc-vrm&family=yokohama&ft:locale=en-US)**

Verify that TPRM works as expected after upgrades and deployments of new applications or integrations by running quick start tests. If you customized TPRM, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US)**

Review the ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes for full descriptions of the features.

-   **[Document Management system](https://www.servicenow.com/docs/access?context=tprm-dms&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

For information on Now Assist skills for TPRM and Document Management, see [ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US) and [Now Assist in Document Intelligence release notes](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-rn&family=zurich&ft:locale=en-US).

-   **[Register of information regulatory packages](https://www.servicenow.com/docs/access?context=tprm-dora-roi&family=zurich&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can now generate regulator-ready Register of Information packages using the Plain-CSV Report Package option on the download page. The ZIP file includes metadata and report folders structured to regulator specifications, with file names containing LEI, entity ID, and release version. This format helps ensure EU DORA compliance and supports automated validation workflows. You can follow the user guide on the Download/Upload request page for suggested steps and permissions.

-   **[Validation framework for RoI](https://www.servicenow.com/docs/access?context=tprm-validation-roi&family=zurich&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can now validate downloaded Register of Information packages using the Plain-CSV Report Package option on the download page against requirements. File format, structure, encoding, naming conventions, and field-level data are validated across multiple tables. If any validation warnings are detected, a validation report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. Validation reports include real-world field labels, rule expressions, and record identifiers. You can cross-reference validation errors using a downloadable Excel master template that mirrors the CSV structure, making it easier to locate and address issues. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data.


</td></tr><tr><td>

Australia

</td><td>

-   **[Generate TPRM issue recommendations](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Support for AI assets in element collection](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, you can add, review, and manage third-party elements, including AI use cases and AI models, in the Elements grid. The grid is available directly on a third-party or engagement record in the Vendor Management Workspace, or embedded in a collection task in the Vendor Management Workspace or third-party portal. Elements linked to multiple engagements reuse existing assessment evidence across linked engagements without requiring a new assessment.

-   **[Internal tasks for due diligence and risk processes](https://www.servicenow.com/docs/access?context=tprm-internal-tasks&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create internal tasks to assign follow-up work to internal users for due diligence and risk processes. Internal tasks aren't visible to third-party contacts and don't appear in the third-party portal.

-   **[DORA register-of-information terminology definitions](https://www.servicenow.com/docs/access?context=tprm-dora-roi-terminology-definitions&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can document register-of-information terminology directly in the Vendor Management Workspace. Term definitions are included in the `B_99.01` CSV export when you generate a Register of Information report.

-   **[Document version comparison for third-party documents](https://www.servicenow.com/docs/access?context=tprm-compare-document-versions&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can use the Document Management System to compare two versions of the same document type collected during third-party assessments. Only DOCX-to-DOCX and DOC-to-DOC formats are supported.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Third-party Risk Management features.

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

-   **[Codes and additional identification information for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-ICT-thirdparty-serv-prov-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **[Function types for ICT third-party service providers](https://www.servicenow.com/docs/access?context=tprm-create-new-function-form&family=yokohama&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.


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


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Third-party and engagement element assessments](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, you can review element-level assessments across all engagements for a third party. Element-level assessments are no longer scoped to a specific engagement. When you scope an assessment, issue, or task to an element, the **Element** field is required. This option is available only when the third party uses the Smart Assessment Engine. Third-party and engagement contacts respond to element-scoped assessments in the third-party portal the same way they respond to engagement-scoped assessments.

-   **[Risk scoring for third-party elements](https://www.servicenow.com/docs/access?context=tprm-monitor-tp-elements&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, element assessment scores roll up through relationship scores calculated from questionnaire-level evidence, replacing the previous entity-based rollup calculation. Engagement and third-party risk-area calculations include assessments sent on linked elements. Linking an element with existing assessment evidence to a new engagement calculates a risk rating for that link automatically, without requiring a new assessment.

-   **[Access external and internal tasks from separate modules](https://www.servicenow.com/docs/access?context=tprm-ws-list-page&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, you can access external and internal tasks from separate modules. The Tasks module is split into **External Tasks** and **Internal Tasks** on the list page. This separates external tasks from the internal task functionality added in element collection.

-   **[Expanded access to reassign Smart Assessment Engine questionnaires](https://www.servicenow.com/docs/access?context=tprm-portal-questionnaire-ownership&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] roles now include the sn\_smart\_asmt.reassign role. Users with these roles can reassign Smart Assessment Engine questionnaires.

-   **[Decimal precision for DORA monetary values](https://www.servicenow.com/docs/access?context=tprm-dora-roi&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role, you can set decimal precision to `-6`, `-3`, `0`, or `2` for monetary value fields. Previously, only `-6`, `-3`, and `0` were supported. This applies to Master Template and CSV downloads. The default precision remains `0`. This change doesn't affect UI display, upload and validation, individual table downloads, or database storage.

-   **[CSV download applies only filtered records when all records are selected](https://www.servicenow.com/docs/access?context=tprm-excel-upload-download-request&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, when a filter is applied to a list and you select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **[Issue generation rules no longer create issues for hidden questions](https://www.servicenow.com/docs/access?context=tprm-generate-issue-rule&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, an issue generation rule that targets a question with a visibility condition no longer creates an issue when that question is isn't visible to the respondent. Previously, the rule could create an issue for a question the respondent never saw.

-   **[Product model record created after SBOM document processing](https://www.servicenow.com/docs/access?context=sbom-activate&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, after a third party submits an SBOM file and processing completes, a product model record is created on the third-party record. The record is visible in the Product Models related list. A plugin dependency is added to support parallel processing.

-   **[Legal person identifier validation warns instead of blocking for non-LEI/EUID codes](https://www.servicenow.com/docs/access?context=tprm-dora-roi&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, after a third-party service provider record with a legal person type and a non-LEI/EUID identification code is submitted, you receive a warning. The save is no longer blocked. This applies to both the Vendor Management Workspace and Excel Upload.

-   **[Notice period fields accept a value of zero](https://www.servicenow.com/docs/access?context=tprm-validation-roi&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.

-   **[Data quality warnings CSV added to CSV ROI report package](https://www.servicenow.com/docs/access?context=tprm-validation-roi&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the CSV report package includes a `Data_Quality_Warnings.csv` file in the `Consolidated_Reports.zip` archive. This file provides supplementary data quality checks beyond the Level 3 \(DPM\) and Level 4 \(LEI\) validations.

These warnings flag potential data inconsistencies — such as duplicate rows, missing assessments, orphaned contracts, supply chain gaps, and criticality conflicts — but don't prevent submission. Addressing them helps maintain data accuracy. Each warning includes the sheet name, row number, contract reference, and a descriptive message.

-   **[Parent record navigation added to DORA third-party, third-party engagement, and contract records](https://www.servicenow.com/docs/access?context=tprm-dora&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a reference field is available on DORA third-party, third-party engagement, and contract records. Use it to navigate back to the related parent record after arriving from a related list. Previously, there was no way to return to the parent record from these pages.

-   **[Excel export for DORA Functions requests no longer fails on large datasets](https://www.servicenow.com/docs/access?context=tprm-dora&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **[Automated quarterly CSV download for Register of Information reports](https://www.servicenow.com/docs/access?context=tprm-dora-roi&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a quarterly scheduled job \(**DORA: Quarterly CSV download**\) generates the CSV Register of Information report for the previous quarter automatically, copying settings from the most recent download request. Previously, a TPR administrator generated this report manually each quarter. The scheduled job is inactive by default; a TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] can navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and activate it before it runs.

-   **[Rank 1 supply chain records update automatically when a contract's service provider changes](https://www.servicenow.com/docs/access?context=tprm-dora&family=brazil&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **[Third party field pre-populated when creating an element from an engagement](https://www.servicenow.com/docs/access?context=tprm-tpe-form&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, the **Third party** field is auto-populated when you create a third-party element from either the third-party record or an engagement's **Elements** tab. Previously, the field was editable and empty in both cases.

-   **[Smart Assessment Engine rating scale available from workspace navigation](https://www.servicenow.com/docs/access?context=tprm-risk-rating-scales-config&family=brazil&ft:locale=en-US)**

After upgrading to version 23.0.7, the SAE default rating scale table is available from the Vendor Management Workspace navigation, under **Assessment Setup**. Previously, this table wasn't accessible from workspace navigation.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Third-party Risk Management features or functionality were removed.

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

Between your current release family and Brazil, some Third-party Risk Management features or functionality were deprecated.

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

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Australia

</td><td>

-   Assessments using entities are no longer supported.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


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


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


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


</td></tr><tr><td>

Australia

</td><td>

-   **Accessibility information**

The Vendor Management Workspace and the third-party portal include accessibility improvements in this release, including improved color contrast, enhanced focus indicators, skip navigation links, and full keyboard navigation.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

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

</td></tr><tr><td>

Australia

</td><td>

-   **Localization information**

Third-party portal strings are externalized and translated for supported languages. Newly introduced features may have incomplete translations.


</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

 Starting with Australia Patch 5, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 -   Reduce manual data entry by using AI to pre‑fill questionnaires for third-party contacts and business owners.
-   Use updated Standardized Information Gathering \(SIG\) questionnaire content for 2026.
-   Automate Software Bill of Materials \(SBOM\) collection, integration, and vulnerability correlation with Unified Security Exposure Management \(USEM\) integration.
-   Manage SAE assessment template versions to prevent changes from affecting in‑flight assessments.
-   Add question-level comments and follow-up capabilities during SAE reviews.
-   Maintain DORA Register of Information accuracy with automatic supply chain cascading updates and duplicate record detection for contractual arrangement and supply chain tables.
-   Validate Legal Entity Identifier \(LEI\) codes against the GLEIF database during Register of Information reporting to identify format errors, checksum failures, and inactive or unissued entities.

 -   Enhance DORA Register of Information reporting with optional currency conversion and third‑party expense aggregation to generate consistent, regulator‑ready reports.
-   Review the simplified third‑party elements process in the due diligence workflow.
-   Access the unified content management module in the Vendor Management Workspace to view a centralized library of smart assessment templates.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

 Review the updated AI experience with three licensing tiers.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=australia&ft:locale=en-US) for more information.

 [Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US)

 Use generative AI to recommend TPRM issues for reviewer validation.

</td></tr><tr><td>

Brazil

</td><td>

-   Assess, score, and monitor risk across your third-party relationships, from initial due diligence through ongoing engagement.
-   Centralize third-party assessments, issue tracking, and remediation in a single workspace.
-   Manage third-party engagements throughout their life cycle with workflows for ongoing oversight and risk management.

 See [September 2026](https://www.servicenow.com/docs/access?context=grc-tprm-rn-2026-09&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

