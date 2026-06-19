---
title: Validate the Register of Information packages
description: Run real-time validation on Register of Information \(RoI\) packages to help ensure compliance with DORA requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/opres-drtp-validate-roi.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Validate the Register of Information packages

Run real-time validation on Register of Information \(RoI\) packages to help ensure compliance with DORA requirements.

## Before you begin

Role required: sn\_oper\_res.manager

Generate a Plain-CSV Reporting Package and an Excel Master Template. For more information, see [Generate a Register of Information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/opres-drtp-gen-roi-pkg.md).

## About this task

Validation is performed automatically when a ZIP file containing RoI CSV templates is uploaded via an Excel download/upload request. The system initiates real-time validation without requiring a separate request type.

Once validation is complete, the system sends an email notification to whoever initiated the request. If validation warnings are detected, both the validation report and the CSV package are attached to the request record. If no issues are found, only the CSV package is included.

The validation report contains mappings to regulator fields such as Template Code, Row Code, and Column Code, along with rule expressions, field labels, and record identifiers. These details help users locate and resolve issues efficiently.

To review and resolve validation errors, download the Excel template from the **Download/Upload Request** page. The template mirrors the CSV structure and includes field definitions, formats, and sample values. Use it to cross-reference the validation report and identify the location and context of each issue.

Validation reports are only generated when errors or warnings are present. If no issues are found, only the CSV package is returned:

-   Fully\_corroborated: All comparison points \(entity name, country, status\) match between the input row and GLEIF.
-   Partially\_corroborated: At least one comparison point mismatches; the row is still uploadable but is flagged for review.
-   Not\_corroborated: The LEI was not found in GLEIF or the input row contradicts authoritative GLEIF data.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Open the request record you want.

3.  Download the validation report from the attachment area of the request record.

    A sample level 4 LEI validation report opened in Microsoft Excel is shown in the example.

    \[Omitted image "level-4-lei-validation-report.png"\] Alt text: Level 4 LEI validation report opened in Microsoft Excel.

    In the report, each row identifies a sheet, row, column from the uploaded package, the LEI checks performed \(format, checksum, GLEIF lookup, status, country match, corroboration\), and a human-readable validation message.

4.  Cross-reference the validation report with the Microsoft Excel template to identify and correct issues.

    If the validation report contains errorCode=INVALID\_VALUE with an errorMessage of "LEI not found in GLEIF database", the identification code value for that branch record is not found in the GLEIF \(Global Legal Entity Identifier Foundation\) registry as shown in the example.

    \[Omitted image "lei-validation-upload-error-messages.png"\] Alt text: LEI validation upload error messages.

    Update the Identification code of the branch field in the source record with a valid 20-character LEI and re-upload the package.

5.  Update the affected records in the system or spreadsheet and re-upload the corrected package for re-validation.


**Parent Topic:**[Configuring Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-dg-resi-party-regi.md)

