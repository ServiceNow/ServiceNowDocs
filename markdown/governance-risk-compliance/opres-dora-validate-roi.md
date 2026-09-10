---
title: Validation framework for Register of Information in Operational Resilience
description: The validation framework helps to verify that RoI packages meet regulatory requirements defined by the DORA.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/opres-dora-validate-roi.html
release: zurich
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 7
breadcrumb: [Exploring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
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

The decimalsMonetary property controls decimal precision for monetary values in the generated RoI package. Enter a negative value to round values to the nearest order of magnitude \(for example, "-3" rounds to the nearest thousand\). Enter a positive value to retain that many decimal places instead of rounding \(for example, "2" retains two decimal places\).

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

## Data quality warnings

Starting with version 23.0.x, several business-rule checks are added to RoI validation for contracts and third-party service providers. Register of Information \(RoI\) data quality warning messages are collected in a dedicated `Data_Quality_Warnings.csv` file included in the `Consolidated_Reports.zip` attachment, in addition to appearing in the request record's message field. The following checks generate data quality warnings during Plain-CSV reporting package generation. These checks generate warnings only; they don't block CSV package generation.

-   Supplier identifier consistency: For the same contract, the service provider code in template B\_02.02 must match the Rank 1 service provider code in template B\_05.02. The type of ICT services in template B\_02.02 must also match the Rank 1 type in template B\_05.02. A mismatch in either field generates a warning.
-   Duplicate Rank 1 supply chain records: Each contract should have exactly one Rank 1 supply chain record. Duplicate Rank 1 records for the same contract generate a warning.
-   Orphaned overarching contracts: A contract with contract type set to **Overarching** must have at least one **Subsequent or associated** contract that references it. If no subsequent contract references an overarching contract, the system generates a warning.
-   Missing overarching contract reference: A contract with contract type \(template B\_02.01, field C0020\) set to **Subsequent or associated** must reference its overarching contract in the corresponding field \(template B\_02.01, field C0030\). If a subsequent contract has no overarching contract reference, the system generates a warning categorized as Missing Overarching Reference. This check is the inverse of the orphaned overarching contracts check above: that check looks for an overarching contract with no subsequent contract pointing to it, and this check looks for a subsequent contract with no overarching contract reference.
-   Missing assessments: A contract reported in template B\_02.01 must have at least one corresponding assessment in template B\_07.01. If a contract has no assessment, the system generates a warning.
-   Missing Rank 1 supply chain records: A contract reported in template B\_02.01 must have at least one corresponding Rank 1 supply chain row in template B\_05.02. This is a defensive check for edge cases such as data migration or backend scripts; a Rank 1 record is normally created automatically when a contract is created. If a contract has no Rank 1 row, the system generates a warning.
-   Supply criticality consistency: A function marked as critical in template B\_06.01 requires matching criticality in related templates, evaluated as two categories of checks against template B\_02.02 fields. Field consistency: sensitiveness of stored data and level of reliance can't both be set to a low value, and the B\_07.01 exit strategy field can't be set to **No**. Conditional mandatory fields: when the function is critical, fields C0100, C0110, C0120, and C0180 become required. When storage of data \(field C0140\) is set to **Yes**, fields C0150 and C0160 also become required. Field C0170 becomes required when the function is critical and storage of data is **Yes**. A missing required field or an inconsistent value generates a warning.
-   Country-specific codes: Legal-person third-party identifiers that use a country-specific code, such as CRN, VAT, NIN, or PNR, instead of an LEI or EUID generate a data quality warning. The record is not blocked. The primary and additional code type fields are evaluated independently. A single record can generate a separate warning for each field if both use a non-LEI/EUID code type. The warning appears in three places: as a field-level message on the **Type of code** fields, in the upload request's result message when importing third parties, and in the `Data_Quality_Warnings.csv` file.

**Note:** Fields `B_02.02.0100` and `B_02.02.0110` accept a value of `0`.

## Common validation issues

Refer to the following guidance to troubleshoot common validation issues when submitting RoI packages.

-   Validation report is missing: The uploaded package contains no errors or warnings. Check the **Result** section of the request. If no issues are found, only the CSV package is returned and no validation report is generated.
-   Missing required fields: One or more required fields are empty or incorrectly formatted. Open the validation report and locate the affected row and column. Use the template to identify the correct field name and expected format. Update the record in the ServiceNow instance or source system and revalidate.
-   Rule expression failures: The data violates one or more business rules defined in the validation framework. Review the rule expression and description in the validation report. Use the record identifier to locate the affected record and correct the data. Common issues include invalid LEI formats, empty currency fields, or missing contract references.
-   Invalid use of “Not applicable” values: These values are used in fields that don’t support them. Check the field definition in the template. Replace “Not applicable” with a valid value or remove it if the field is required. Revalidate the updated package.
-   Validation report is difficult to interpret: The report lacks context or field labels are unclear. Download the template and use it to cross-reference the row number, sheet name, and record identifier. This helps locate the affected record and understand the validation error in context.
-   File size or encoding issues: The uploaded ZIP file exceeds the 5 MB limit or uses unsupported encoding. Compress the file to meet the size requirement and ensure all CSV files use UTF-8 encoding. Re-upload the corrected package.

For more information, see [Validate the Register of Information packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/opres-drtp-validate-roi.md).

**Parent Topic:**[Exploring Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/exploring-digi-resi-third-party-registers.md)

