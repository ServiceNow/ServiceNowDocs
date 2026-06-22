---
title: Combined Third-party Risk Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Third-party Risk Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-thirdpartyriskmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Third-party Risk Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Third-party Risk Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Third-party Risk Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Third-party Risk Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=zurich&ft:locale=en-US).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td></tr><tr><td>

Australia

</td><td>

If you're a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don't run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

 After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn't reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

 For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://www.servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=australia&ft:locale=en-US).

 For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

 After upgrading to version 22.3.3, the `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles. During upgrade, most users are automatically migrated to new feature‑specific roles. Users with custom role combinations may not be migrated automatically and require manual review before the grace period ends.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US)**

Review the Now Assist for Third-party Risk Management \(TPRM\) \(TPRM\) release notes for full descriptions of the features.

-   **[Document Management system](https://www.servicenow.com/docs/access?context=tprm-dms&family=zurich&ft:locale=en-US)**

Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

For information on Now Assist skills for TPRM and Document Management, see [Now Assist for Third-party Risk Management \(TPRM\) release notes](https://www.servicenow.com/docs/access?context=now-assist-for-tprm-rn&family=zurich&ft:locale=en-US) and [Now Assist in Document Intelligence release notes](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-rn&family=zurich&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

</td><td>

-   **[AI-assisted questionnaire pre-fill](https://www.servicenow.com/docs/access?context=tprm-dms-sae&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3 and activating the Now Assist for Third-party Risk Management \(TPRM\) application, you can use uploaded documents and responses from previous assessments to generate suggested questionnaire responses with source citations. For internal assessments you need the snc\_internal role. For external assessments, primary contacts can complete all assessment response actions; secondary contacts must be assigned read and write access.

-   **[Software Bill of Materials \(SBOM\) support](https://www.servicenow.com/docs/access?context=tprm-sbom-exploring&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2 and installing the required SBOM applications, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or third-party risk assessor role \[sn\_vdr\_risk\_asmt.vendor\_risk\_assessor\], you can collect and manage SBOM data to support regulatory disclosure requirements.

-   **[Standardized Information Gathering \(SIG\) 2026 questionnaires](https://www.servicenow.com/docs/access?context=tprm-sig-use-and-support&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.0, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can use updated SIG Full, SIG Core, and SIG Lite templates for 2026 with expanded coverage across major security and privacy frameworks. Existing SIG questionnaire versions remain available. In‑flight assessments aren't affected.

-   **[Smart Assessment template versioning](https://www.servicenow.com/docs/access?context=tprm-sae-using&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can manage SAE template lifecycles using explicit versioning so that in-flight assessments use the version that was active when they were created.

-   **[Legal Entity Identifier \(LEI\) validation for DORA reporting](https://www.servicenow.com/docs/access?context=tprm-valid-lei&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can validate Legal Entity Identifier codes against the GLEIF database to support regulatory accuracy in Register of Information reporting. For descriptions of validation results and report columns, see [Level 4 LEI Validation Report columns](https://www.servicenow.com/docs/access?context=tprm-lei-validation-report&family=australia&ft:locale=en-US).

-   **[Generate aggregate regulatory reports in local currencies](https://www.servicenow.com/docs/access?context=tprm-dora-currency-aggregation&family=australia&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://www.servicenow.com/docs/access?context=tprm-integrating-ucm&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


 -   **[Generate TPRM issue recommendations](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Third-party Risk Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

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

-   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&family=zurich&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


</td></tr><tr><td>

Australia

</td><td>

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

-   **[Simplified third-party element process](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Third-party Risk Management features or functionality were removed.

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

-   Assessments using entities are no longer supported.
-   The `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles.
-   The `scoring_rule` and `scoring_rule_ref` fields are removed from assessment forms and UI sections. Custom scripts or integrations that reference these fields must be updated.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Third-party Risk Management features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Third-party Risk Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Third-party Risk Management by requesting it from ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Third-party Risk Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Third-party Risk Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for the Vendor Management Workspace and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

The Vendor Management Workspace and the third-party portal include accessibility improvements in this release, including improved color contrast, enhanced focus indicators, skip navigation links, full keyboard navigation, and ARIA attribute updates for screen reader compatibility.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Third-party Risk Management we have noted them here.

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

Third-party portal strings are externalized and translated for supported languages. Newly introduced features may have incomplete translations.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Third-party Risk Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

 [Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US)

 Use generative AI to recommend TPRM issues for reviewer validation.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

 Review the updated AI experience with three licensing tiers.

 See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

