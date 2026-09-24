---
title: Combined Third-party Risk Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Third-party Risk Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-thirdpartyriskmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 21
breadcrumb: [Products combined by family]
---

# Combined Third-party Risk Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Third-party Risk Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Third-party Risk Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Third-party Risk Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Australia

</td><td>

-   **[Extended AI model support for Now Assist for TPRM](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-tprm&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.4, ServiceNow Otto for Third-party Risk Management \(TPRM\) supports Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models in addition to previously supported models. Model availability depends on your ServiceNow Otto for Third-party Risk Management \(TPRM\) subscription, providing greater flexibility when selecting the AI model that meets your requirements.


 -   **[AI-assisted questionnaire pre-fill](https://www.servicenow.com/docs/access?context=tprm-dms-sae&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3 and activating the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use uploaded documents and responses from previous assessments to generate suggested questionnaire responses with source citations. For internal assessments, the snc\_internal role is required. For external assessments, primary contacts can complete all assessment response actions; secondary contacts must be assigned read and write access.

-   **[Software Bill of Materials \(SBOM\) support](https://www.servicenow.com/docs/access?context=tprm-sbom-exploring&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2 and installing the required SBOM applications, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or third-party risk assessor role \[sn\_vdr\_risk\_asmt.vendor\_risk\_assessor\], you can collect and manage SBOM data to support regulatory disclosure requirements.

-   **[Standardized Information Gathering \(SIG\) 2026 questionnaires](https://www.servicenow.com/docs/access?context=tprm-sig-use-and-support&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.0, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can use updated SIG Full, SIG Core, and SIG Lite templates for 2026 with expanded coverage across major security and privacy frameworks. Existing SIG questionnaire versions remain available. In‑flight assessments aren't affected.

-   **[Smart Assessment template versioning](https://www.servicenow.com/docs/access?context=tprm-sae-using&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can manage SAE template lifecycles using explicit versioning so that in-flight assessments use the version that was active when they were created.

-   **[Legal Entity Identifier \(LEI\) validation for DORA reporting](https://www.servicenow.com/docs/access?context=tprm-valid-lei&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can validate Legal Entity Identifier codes against the GLEIF database to support regulatory accuracy in Register of Information reporting. For descriptions of validation results and report columns, see [Level 4 LEI Validation Report columns](https://www.servicenow.com/docs/access?context=tprm-lei-validation-report&family=australia&ft:locale=en-US).


 -   **[Generate TPRM issue recommendations](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


 -   **[Generate aggregate regulatory reports in local currencies](https://www.servicenow.com/docs/access?context=tprm-dora-currency-aggregation&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://www.servicenow.com/docs/access?context=tprm-integrating-ucm&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


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

Australia

</td><td>

-   **[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)**

Starting with Australia Patch 5, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


 -   **[Default AI model for issue recommendation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-tprm&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.4, the issue recommendation skill in ServiceNow Otto for Third-party Risk Management \(TPRM\) uses Azure OpenAI gpt-4-5-mini as the default model. This update changes the default model for issue recommendations. You can select alternative models, including the newly supported Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini, based on your requirements.

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[Improved handling of skipped conditional questions in SAE assessments](https://www.servicenow.com/docs/access?context=tprm-sae-using&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, Smart Assessment Engine assessments hide conditional questions that are skipped based on response logic. Sections that contain skipped questions are visually de‑emphasized, and assessments render in a continuous scroll layout.This change affects the assessment review experience only and does not change assessment logic, scoring, or response data.

-   **[Comments field in the third‑party portal saves when you leave the field](https://www.servicenow.com/docs/access?context=vendor-portal&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, the comments field in the third‑party portal saves when you leave the field rather than on every keystroke.

-   **[Issue indicators in the third-party portal shown only after submission](https://www.servicenow.com/docs/access?context=vendor-portal&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, issue indicators appear in the third‑party portal only after an issue is submitted to the third party and the **Visible in third‑party portal** field is selected. Previously, indicators were visible before submission when the field was selected.


 -   **[Consolidated assessment email notifications](https://www.servicenow.com/docs/access?context=set_sys_props_for_email&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, external assessment‑related email notifications are sent as a single consolidated summary instead of individual per‑event messages. Users can configure notification frequency, detail level, and delivery channel in their notification preferences. Multi‑language templates are available.

-   **[Assessment count mechanism updated in the third-party portal](https://www.servicenow.com/docs/access?context=vendor-portal&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, engagement assessment counts in the third-party portal include only active, pending, and in‑progress assessments. Previously, counts included inactive and canceled assessments.

-   **[Inactive metrics excluded when copying assessment responses](https://www.servicenow.com/docs/access?context=tprm-assessing-tpr&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, inactive and retired metrics are excluded when copying responses between assessments. Previously, copying responses could include inactive metrics, causing scoring errors.

-   **[Type of ICT services changes cascade to supply chain in DORA reporting](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, when the Type of ICT services value is updated on a Contractual Arrangements – Specific Information \(B.02.02\) record, the ICT service supply chain \(B.05.02\) is now updated automatically. If a Type of ICT services value is removed from a Specific Information record, the corresponding supply chain records for Rank 1 and higher ranks are also deleted automatically. Previously, Rank 1 supply chain records were generated when the Specific Information record was first created, but subsequent changes or removals did not propagate to the supply chain, requiring manual correction.

-   **[Duplicate contractual arrangements detected and warned in DORA Register of Information](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, duplicate records in the Contractual Arrangements – Specific Information \(B.02.02\) table are now detected and handled across three scenarios. When saving a contractual arrangement from the UI, a business rule checks eight composite key fields and blocks the save if a duplicate is found. During Excel upload, duplicate rows are rejected and logged to the upload error report. During CSV package download, duplicate rows in B.02.02 are flagged in the DORA request record's error log; duplicates are warned but not removed from the generated CSV.

-   **[Duplicate supply chain rows warned during DORA CSV package download](https://www.servicenow.com/docs/access?context=tprm-drtp-roi-packages&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, during CSV package download, duplicate rows in the ICT service supply chains \(B.05.02\) table are now detected and a warning is added to the request record. This applies to both Rank 1 supply chain records, which are auto-generated from Specific Information records, and higher-ranked records. Additionally, when the Storage of data field is set to No on a contractual arrangement, associated location field values are now cleared automatically.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Fields added to Create New Excel download/upload request form](https://www.servicenow.com/docs/access?context=tprm-create-report-aggregate-expenses&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, the **Enable currency conversion** and **Enable third‑party total expense aggregation** fields are available on the Excel download/upload request page. When creating Excel Master Template or Plain‑CSV Reporting Package requests, you can configure these options directly on the form.

-   **[TPRM Unified content management page](https://www.servicenow.com/docs/access?context=tprm-ws-ucm-page&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2 and installing the Unified Content Management application, the unified content management module is available in the Vendor Management Workspace.


 -   **[Simplified third-party element process](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


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

Australia

</td><td>

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

 -   The `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles.
-   The `scoring_rule` and `scoring_rule_ref` fields are removed from assessment forms and UI sections. Custom scripts or integrations that reference these fields must be updated.

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

Australia

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Note:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


**Note:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

Review details on accessibility information for Third-party Risk Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

