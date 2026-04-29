---
title: Validation framework for Register of Information in Operational Resilience
description: The validation framework helps to verify that RoI packages meet regulatory requirements defined by the DORA.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Validation framework for Register of Information in Operational Resilience

The validation framework helps to verify that RoI packages meet regulatory requirements defined by the DORA.

## Validation overview

The validation framework for the Digital Resilience Third-party Information Register application ensures that downloaded RoI packages comply with the structural, formatting, and data integrity requirements defined by the DORA. It supports a real-time, three-level validation system that automatically checks for technical accuracy, regulatory alignment, and business rule compliance during the upload process.

-   Level 1 \(Technical checks\): 29 rules validating file encoding, structure, and naming.
-   Level 2 \(Data package mode technical checks\): 12 rules ensuring template and schema alignment.
-   Level 3 \(Data package model business rules\): 70 rules verifying regulatory logic and field dependencies.

**Note:** The Data Package Model is used to structure and validate RoI packages.

The DPM business validation rules and report.json, reportPackage.json, FrameworkCodeModuleVersion properties enable Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] to view and maintain validation logic and configuration settings for CSV reporting and automated validation. Third-party risk admins can access these properties by navigating to **All** &gt; **Digital Operational Resilience Management** and then selecting **Properties** or **DPM Business Validation Rules**.

## Validation process

Validation is now performed automatically during the upload of RoI CSV files. As soon as the ZIP package is uploaded via an Excel download/upload request, the system initiates real-time validation without requiring a separate request type. The system performs checks across multiple dimensions:

-   File-level validation: Ensures correct encoding, naming conventions, and file structure.
-   Template-level validation: Verifies that required templates are present and formatted correctly.
-   Field-level validation: Applies rule expressions to check for missing values, incorrect formats, and invalid references.

Validation results are returned in a downloadable report that includes:

-   Mappings to regulator fields such as Template Code, Row Code, and Column Code.
-   Rule expressions and descriptions.
-   Real-world field labels and record identifiers.
-   Row-level error summaries.

Operational Resilience managers \(sn\_oper\_res.manager\) can validate downloaded RoI packages using the same Plain-CSV Report Package option. After a validation report is generated for a Register of Information \(RoI\) package, the system automatically sends an email notification to whoever initiated the download or upload request. This email alerts the user that the process has completed and provides access to the results. If validation warnings are detected, both the validation report and the CSV package are attached to the request record. If no issues are found, only the CSV package is included. This automated notification ensures timely awareness and facilitates efficient follow-up actions for compliance and data correction workflows.

To assist with error resolution, users can cross-reference the validation report with downloadable templates that mirror the CSV structure. These templates help identify the location and context of each issue, making it easier to correct data in the ServiceNow instance or source system. Validation reports are only generated when errors or warnings are detected. If no issues are found, only the CSV package is returned.

To improve troubleshooting, the system maps rule expressions to real-world field labels and record identifiers. Even when malformed data is uploaded, the validation API returns meaningful error messages to help users identify and resolve issues efficiently.

Excel templates are available for download from the **Download/Upload Request** page. These templates mirror the expected CSV structure and provide field definitions, formats, and sample values to assist with validation and error resolution.

**Important:** The Operational Resilience administrators \(sn\_oper\_res.admin\) and managers \(sn\_oper\_res.managers\) can perform the validation tasks.

## Common validation issues

Refer to the following guidance to troubleshoot common validation issues when submitting RoI packages.

-   Validation report is missing: The uploaded package contains no errors or warnings. Check the **Result** section of the request. If no issues are found, only the CSV package is returned and no validation report is generated.
-   Missing required fields: One or more required fields are empty or incorrectly formatted. Open the validation report and locate the affected row and column. Use the template to identify the correct field name and expected format. Update the record in the ServiceNow instance or source system and revalidate.
-   Rule expression failures: The data violates one or more business rules defined in the validation framework. Review the rule expression and description in the validation report. Use the record identifier to locate the affected record and correct the data. Common issues include invalid LEI formats, empty currency fields, or missing contract references.
-   Invalid use of “Not applicable” values: These values are used in fields that don’t support them. Check the field definition in the template. Replace “Not applicable” with a valid value or remove it if the field is required. Revalidate the updated package.
-   Validation report is difficult to interpret: The report lacks context or field labels are unclear. Download the template and use it to cross-reference the row number, sheet name, and record identifier. This helps locate the affected record and understand the validation error in context.
-   File size or encoding issues: The uploaded ZIP file exceeds the 5 MB limit or uses unsupported encoding. Compress the file to meet the size requirement and ensure all CSV files use UTF-8 encoding. Re-upload the corrected package.

For more information, see [Validate the Register of Information packages](../task/opres-drtp-validate-roi.md).

**Parent Topic:**[Exploring Digital resilience third-party registers](exploring-digi-resi-third-party-registers.md)

