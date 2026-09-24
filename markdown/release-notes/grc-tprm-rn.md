---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management application provides a centralized process for managing third-party engagement portfolios, assessing and scoring risk, and driving remediation. See the following sections for release notes by version. Version 23.0 adds AI asset support in element collection, DORA register-of-information terminology, and document version comparison. It also updates element assessments, risk scoring, and notifications, and fixes SBOM processing issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-tprm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [Third-Party Risk Management, TPRM, Third-Party Risk Management, TPRM, element collection, AI assets, AI use cases, AI models, DORA, register of information, document version comparison, Document Management System, Smart Assessment Engine, SAE, questionnaire reassignment, risk scoring, internal tasks, external tasks, SBOM, issue generation, third-party portal, due diligence]
audience: administrator
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management application provides a centralized process for managing third-party engagement portfolios, assessing and scoring risk, and driving remediation. See the following sections for release notes by version.

## About Third-party Risk Management

-   Assess, score, and monitor risk across your third-party relationships, from initial due diligence through ongoing engagement.
-   Centralize third-party assessments, issue tracking, and remediation in a single workspace.
-   Manage third-party engagements throughout their life cycle with workflows for ongoing oversight and risk management.

See [September 2026](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-tprm-rn.md) for more information.

## Activation and other requirements

**Note:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.

    Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property makes the Smart Assessment Engine \(SAE\) the default assessment engine and replaces the legacy experience.

    **Warning:** Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property is irreversible. Set this property in a non-production instance and test thoroughly before enabling it in production.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## September 2026

Version 23.0 adds AI asset support in element collection, DORA register-of-information terminology, and document version comparison. It also updates element assessments, risk scoring, and notifications, and fixes SBOM processing issues.

### What's new

-   **[Support for AI assets in element collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

    After upgrading to version 23.0.7, you can add, review, and manage third-party elements, including AI use cases and AI models, in the Elements grid. The grid is available directly on a third-party or engagement record in the Vendor Management Workspace, or embedded in a collection task in the Vendor Management Workspace or third-party portal. Elements linked to multiple engagements reuse existing assessment evidence across linked engagements without requiring a new assessment.

-   **[Internal tasks for due diligence and risk processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-internal-tasks.md)**

    After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create internal tasks to assign follow-up work to internal users for due diligence and risk processes. Internal tasks aren't visible to third-party contacts and don't appear in the third-party portal.

-   **[DORA register-of-information terminology definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi-terminology-definitions.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can document register-of-information terminology directly in the Vendor Management Workspace. Term definitions are included in the `B_99.01` CSV export when you generate a Register of Information report.

-   **[Document version comparison for third-party documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-compare-document-versions.md)**

    After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can use the Document Management System to compare two versions of the same document type collected during third-party assessments. Only DOCX-to-DOCX and DOC-to-DOC formats are supported.


### What's changed

-   **[Third-party and engagement element assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

    After upgrading to version 23.0.7, you can review element-level assessments across all engagements for a third party. Element-level assessments are no longer scoped to a specific engagement. When you scope an assessment, issue, or task to an element, the **Element** field is required. This option is available only when the third party uses the Smart Assessment Engine. Third-party and engagement contacts respond to element-scoped assessments in the third-party portal the same way they respond to engagement-scoped assessments.

-   **[Risk scoring for third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

    After upgrading to version 23.0.7, element assessment scores roll up through relationship scores calculated from questionnaire-level evidence, replacing the previous entity-based rollup calculation. Engagement and third-party risk-area calculations include assessments sent on linked elements. Linking an element with existing assessment evidence to a new engagement calculates a risk rating for that link automatically, without requiring a new assessment.

-   **[Access external and internal tasks from separate modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-ws-list-page.md)**

    After upgrading to version 23.0.7, you can access external and internal tasks from separate modules. The Tasks module is split into **External Tasks** and **Internal Tasks** on the list page. This separates external tasks from the internal task functionality added in element collection.

-   **[Expanded access to reassign Smart Assessment Engine questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-portal-questionnaire-ownership.md)**

    After upgrading to version 23.0.7, the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] roles now include the sn\_smart\_asmt.reassign role. Users with these roles can reassign Smart Assessment Engine questionnaires.

-   **[Decimal precision for DORA monetary values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role, you can set decimal precision to `-6`, `-3`, `0`, or `2` for monetary value fields. Previously, only `-6`, `-3`, and `0` were supported. This applies to Master Template and CSV downloads. The default precision remains `0`. This change doesn't affect UI display, upload and validation, individual table downloads, or database storage.

-   **[CSV download applies only filtered records when all records are selected](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-excel-upload-download-request.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, when a filter is applied to a list and you select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **[Issue generation rules no longer create issues for hidden questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-generate-issue-rule.md)**

    After upgrading to version 23.0.7, an issue generation rule that targets a question with a visibility condition no longer creates an issue when that question is isn't visible to the respondent. Previously, the rule could create an issue for a question the respondent never saw.

-   **[Product model record created after SBOM document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sbom-activate.md)**

    After upgrading to version 23.0.7, after a third party submits an SBOM file and processing completes, a product model record is created on the third-party record. The record is visible in the Product Models related list. A plugin dependency is added to support parallel processing.

-   **[Legal person identifier validation warns instead of blocking for non-LEI/EUID codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, after a third-party service provider record with a legal person type and a non-LEI/EUID identification code is submitted, you receive a warning. The save is no longer blocked. This applies to both the Vendor Management Workspace and Excel Upload.

-   **[Notice period fields accept a value of zero](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.

-   **[Data quality warnings CSV added to CSV ROI report package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the CSV report package includes a `Data_Quality_Warnings.csv` file in the `Consolidated_Reports.zip` archive. This file provides supplementary data quality checks beyond the Level 3 \(DPM\) and Level 4 \(LEI\) validations.

    These warnings flag potential data inconsistencies — such as duplicate rows, missing assessments, orphaned contracts, supply chain gaps, and criticality conflicts — but don't prevent submission. Addressing them helps maintain data accuracy. Each warning includes the sheet name, row number, contract reference, and a descriptive message.

-   **[Parent record navigation added to DORA third-party, third-party engagement, and contract records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a reference field is available on DORA third-party, third-party engagement, and contract records. Use it to navigate back to the related parent record after arriving from a related list. Previously, there was no way to return to the parent record from these pages.

-   **[Excel export for DORA Functions requests no longer fails on large datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **[Automated quarterly CSV download for Register of Information reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a quarterly scheduled job \(**DORA: Quarterly CSV download**\) generates the CSV Register of Information report for the previous quarter automatically, copying settings from the most recent download request. Previously, a TPR administrator generated this report manually each quarter. The scheduled job is inactive by default; a TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] can navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and activate it before it runs.

-   **[Rank 1 supply chain records update automatically when a contract's service provider changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **[Third party field pre-populated when creating an element from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-tpe-form.md)**

    After upgrading to version 23.0.7, the **Third party** field is auto-populated when you create a third-party element from either the third-party record or an engagement's **Elements** tab. Previously, the field was editable and empty in both cases.

-   **[Smart Assessment Engine rating scale available from workspace navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-risk-rating-scales-config.md)**

    After upgrading to version 23.0.7, the SAE default rating scale table is available from the Vendor Management Workspace navigation, under **Assessment Setup**. Previously, this table wasn't accessible from workspace navigation.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


