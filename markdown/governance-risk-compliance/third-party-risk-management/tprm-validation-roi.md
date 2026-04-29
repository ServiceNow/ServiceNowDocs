---
title: Validation framework for Register of Information
description: The validation framework helps ensure that RoI packages meet regulatory requirements defined by the DORA.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [DORA validation, RoI package, third-party risk, compliance]
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Validation framework for Register of Information

The validation framework helps ensure that RoI packages meet regulatory requirements defined by the DORA.

## Validation overview

The validation framework for the Digital Resilience Third-party Information Register application helps ensure that downloaded RoI packages comply with the structural, formatting, and data integrity requirements defined by the DORA. It supports a real-time, three-level validation system that automatically checks for technical accuracy, regulatory alignment, and business rule compliance during the upload process.

-   Level 1 \(Technical checks\): 29 rules validating file encoding, structure, and naming.
-   Level 2 \(Data package mode technical checks\): 12 rules ensuring template and schema alignment.
-   Level 3 \(Data package model business rules\): 70 rules verifying regulatory logic and field dependencies.

**Note:** The Data Package Model is used to structure and validate RoI packages.

The DPM business validation rules and report.json, reportPackage.json, FrameworkCodeModuleVersion properties enable Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] to view and maintain validation logic and configuration settings for CSV reporting and automated validation. Third-party risk admins can access these properties by navigating to **All** &gt; **Digital Operational Resilience Management** and then selecting **Properties** or **DPM Business Validation Rules**.

## Validation process

Validation is performed automatically when a Register of Information \(RoI\)Plain-CSV reporting package is uploaded. As soon as the ZIP package is uploaded using a download/upload request, the system initiates real-time validation without requiring a separate request type. The system performs checks across multiple dimensions:

-   File-level validation: Ensures correct encoding, naming conventions, and file structure.
-   Template-level validation: Verifies that required templates are present and formatted correctly.
-   Field-level validation: Applies rule expressions to check for missing values, incorrect formats, and invalid references.

Validation results are returned in a downloadable report that includes:

-   Mappings to regulator fields such as Template Code, Row Code, and Column Code.
-   Rule expressions and descriptions.
-   Real-world field labels and record identifiers.
-   Row-level error summaries.

Third-party risk managers \(sn\_vdr\_risk\_asmt.vendor\_manager\) can review downloaded RoI packages using the same Plain-CSV Report Package option. After a validation report is generated for a Register of Information \(RoI\) package, the system automatically sends an email notification to whoever initiated the download or upload request. This email alerts the user that the process has been completed and provides access to the results. If validation warnings are detected, both the validation report and the CSV package are attached to the request record. If no issues are found, only the CSV package is included. This automated notification ensures timely awareness and facilitates efficient follow-up actions for compliance and data correction workflows.

Validation checks help identify structural and business‑rule issues based on DORA‑aligned specifications. Validation results do not represent a regulatory determination, and supervisory authorities may apply additional or updated checks when reviewing submitted data.

To assist with error resolution, you can cross-reference the validation report with downloadable master templates that mirror the CSV structure. These templates help identify the location and context of each issue, making it easier to correct data in the ServiceNow instance or source system. Validation reports are only generated when errors or warnings are detected. If no issues are found, only the CSV package is returned.

To improve troubleshooting, the system maps rule expressions to real-world field labels and record identifiers. Even when malformed data is uploaded, the validation API returns meaningful error messages to help you identify and resolve issues efficiently.

Excel master templates are available for download from the **Download/Upload Request** page. These templates mirror the expected CSV structure and provide field definitions, formats, and sample values to assist with validation and error resolution.

**Important:** Only users with the TPR admin \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can perform validation tasks.

## Common validation issues

Refer to the following guidance to troubleshoot common validation issues when submitting RoI packages.

-   Validation report is missing: The uploaded package contains no errors or warnings. Check the **Result** section of the request. If no issues are found, only the CSV package is returned and no validation report is generated.
-   Missing required fields: One or more required fields are empty or incorrectly formatted. Open the validation report and locate the affected row and column. Use the master template to identify the correct field name and expected format. Update the record in the ServiceNow instance or source system and revalidate.
-   Rule expression failures: The data violates one or more business rules defined in the validation framework. Review the rule expression and description in the validation report. Use the record identifier to locate the affected record and correct the data. Common issues include invalid LEI formats, empty currency fields, or missing contract references.
-   Invalid use of “Not applicable” values: These values are used in fields that don’t support them. Check the field definition in the master template. Replace “Not applicable” with a valid value or remove it if the field is required. Revalidate the updated package.
-   Validation report is difficult to interpret: The report lacks context or field labels are unclear. Download the master template and use it to cross-reference the row number, sheet name, and record identifier. This helps locate the affected record and understand the validation error in context.
-   File size or encoding issues: The uploaded ZIP file exceeds the 5-MB limit or uses unsupported encoding. Compress the file to meet the size requirement and verify all CSV files use UTF-8 encoding. Re-upload the corrected package.

