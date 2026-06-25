---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 10
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

## Third-party Risk Management highlights for the Australia release

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

[Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md)

Use generative AI to recommend TPRM issues for reviewer validation.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

Review the updated AI experience with three licensing tiers.

See [Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md) for more information.

**Important:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Third-party Risk Management to Australia

If you're a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don't run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn't reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

After upgrading to version 22.3.3, the `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles. During upgrade, most users are automatically migrated to new feature‑specific roles. Users with custom role combinations may not be migrated automatically and require manual review before the grace period ends.

## New in the Australia release

-   **[AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-dms-sae.md)**

    After upgrading to version 22.3.3 and activating the Now Assist for Third-party Risk Management \(TPRM\) application, you can use uploaded documents and responses from previous assessments to generate suggested questionnaire responses with source citations. For internal assessments you need the snc\_internal role. For external assessments, primary contacts can complete all assessment response actions; secondary contacts must be assigned read and write access.

-   **[Software Bill of Materials \(SBOM\) support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sbom-exploring.md)**

    After upgrading to version 22.3.2 and installing the required SBOM applications, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or third-party risk assessor role \[sn\_vdr\_risk\_asmt.vendor\_risk\_assessor\], you can collect and manage SBOM data to support regulatory disclosure requirements.

-   **[Standardized Information Gathering \(SIG\) 2026 questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sig-use-and-support.md)**

    After upgrading to version 22.3.0, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can use updated SIG Full, SIG Core, and SIG Lite templates for 2026 with expanded coverage across major security and privacy frameworks. Existing SIG questionnaire versions remain available. In‑flight assessments aren't affected.

-   **[Smart Assessment template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sae-using.md)**

    After upgrading to version 22.3.3, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can manage SAE template lifecycles using explicit versioning so that in-flight assessments use the version that was active when they were created.

-   **[Legal Entity Identifier \(LEI\) validation for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-valid-lei.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can validate Legal Entity Identifier codes against the GLEIF database to support regulatory accuracy in Register of Information reporting. For descriptions of validation results and report columns, see [Level 4 LEI Validation Report columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-lei-validation-report.md).

-   **[Generate aggregate regulatory reports in local currencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-dora-currency-aggregation.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-integrating-ucm.md)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


-   **[Generate issue recommendations for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-recommendation-tprm-issue.md)**

    After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


## UI changes

-   **[Improved handling of skipped conditional questions in SAE assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sae-using.md)**

    After upgrading to version 22.3.3, Smart Assessment Engine assessments hide conditional questions that are skipped based on response logic. Sections that contain skipped questions are visually de‑emphasized, and assessments render in a continuous scroll layout.

    This change affects the assessment review experience only and does not change assessment logic, scoring, or response data.

-   **[Comments field in the third‑party portal saves when you leave the field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.2, the comments field in the third‑party portal saves when you leave the field rather than on every keystroke.

-   **[Issue indicators in the third-party portal shown only after submission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.2, issue indicators appear in the third‑party portal only after an issue is submitted to the third party and the **Visible in third‑party portal** field is selected. Previously, indicators were visible before submission when the field was selected.

-   **[Fields added to Create New Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-create-report-aggregate-expenses.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, the **Enable currency conversion** and **Enable third‑party total expense aggregation** fields are available on the Excel download/upload request page. When creating Excel Master Template or Plain‑CSV Reporting Package requests, you can configure these options directly on the form.

-   **[TPRM Unified content management page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-ws-ucm-page.md)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, the unified content management module is available in the Vendor Management Workspace.


## Changed in this release

-   **[Consolidated assessment email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set_sys_props_for_email.md)**

    After upgrading to version 22.3.3, external assessment‑related email notifications are sent as a single consolidated summary instead of individual per‑event messages. Users can configure notification frequency, detail level, and delivery channel in their notification preferences. Multi‑language templates are available.

-   **[Assessment count mechanism updated in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.3, engagement assessment counts in the third-party portal include only active, pending, and in‑progress assessments. Previously, counts included inactive and canceled assessments.

-   **[Inactive metrics excluded when copying assessment responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-assessing-tpr.md)**

    After upgrading to version 22.3.3, inactive and retired metrics are excluded when copying responses between assessments. Previously, copying responses could include inactive metrics, causing scoring errors.

-   **[Type of ICT services changes cascade to supply chain in DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, when the Type of ICT services value is updated on a Contractual Arrangements – Specific Information \(B.02.02\) record, the ICT service supply chain \(B.05.02\) is now updated automatically. If a Type of ICT services value is removed from a Specific Information record, the corresponding supply chain records for Rank 1 and higher ranks are also deleted automatically. Previously, Rank 1 supply chain records were generated when the Specific Information record was first created, but subsequent changes or removals did not propagate to the supply chain, requiring manual correction.

-   **[Duplicate contractual arrangements detected and warned in DORA Register of Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, duplicate records in the Contractual Arrangements – Specific Information \(B.02.02\) table are now detected and handled across three scenarios. When saving a contractual arrangement from the UI, a business rule checks eight composite key fields and blocks the save if a duplicate is found. During Excel upload, duplicate rows are rejected and logged to the upload error report. During CSV package download, duplicate rows in B.02.02 are flagged in the DORA request record's error log; duplicates are warned but not removed from the generated CSV.

-   **[Duplicate supply chain rows warned during DORA CSV package download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-roi-packages.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, during CSV package download, duplicate rows in the ICT service supply chains \(B.05.02\) table are now detected and a warning is added to the request record. This applies to both Rank 1 supply chain records, which are auto-generated from Specific Information records, and higher-ranked records. Additionally, when the Storage of data field is set to No on a contractual arrangement, associated location field values are now cleared automatically.

-   **[Simplified third-party element process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-workflow-in-workspace.md)**

    After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Removed in this release

-   Assessments using entities are no longer supported.
-   The `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles.
-   The `scoring_rule` and `scoring_rule_ref` fields are removed from assessment forms and UI sections. Custom scripts or integrations that reference these fields must be updated.

## Accessibility information

The Vendor Management Workspace and the third-party portal include accessibility improvements in this release, including improved color contrast, enhanced focus indicators, skip navigation links, full keyboard navigation, and ARIA attribute updates for screen reader compatibility.

## Localization information

Third-party portal strings are externalized and translated for supported languages. Newly introduced features may have incomplete translations.

## Activation information

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-opres-landing-page.md)**

    Operational Resilience helps organizations respond to adverse operational events by anticipating, preventing, recovering from, and adapting to such events.

-   **[Operational Resilience Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/working-in-opres-ws.md)**

    Use Operational Resilience Workspace to manage your resilience tasks and monitor resilience metrics from a single dashboard.

-   **[GRC Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-overview.md)**

    Use Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce your reaction time from days to minutes.

-   **[GRC Risk Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-workspace.md)**

    The Risk Workspace in the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for risk-related activities.

-   **[Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-asmnt-engine-landing-page.md)**

    The ServiceNow® Smart Assessment Engine \(SAE\) application helps you to reduce the manual burden and costs of your assessment processes through automation.


-   **[Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-tprm-upgrade-info.md)**  
ServiceNow® Third-party Risk Management application upgrade information for the Australia release.

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

