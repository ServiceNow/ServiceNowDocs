---
title: Validate Legal Entity Identifier codes for DORA reporting
description: Review and resolve Legal Entity Identifier \(LEI\) validation results for DORA Register of Information reporting. LEI validation runs automatically during Plain-CSV Reporting Package generation and Microsoft Excel upload to verify that LEI codes in the digital resilience registers exist in the GLEIF database and have an active and issued status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-valid-lei.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 5
keywords: [LEI validation, GLEIF, DORA, Register of Information, Level 4]
breadcrumb: [Validation framework for RoI, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Validate Legal Entity Identifier codes for DORA reporting

Review and resolve Legal Entity Identifier \(LEI\) validation results for DORA Register of Information reporting. LEI validation runs automatically during Plain-CSV Reporting Package generation and Microsoft Excel upload to verify that LEI codes in the digital resilience registers exist in the GLEIF database and have an active and issued status.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

Generate a Plain-CSV Reporting Package. For more information, see [Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md).

## About this task

Level 4 LEI validation checks LEI codes in the Digital resilience third-party registers against the Global Legal Entity Identifier Foundation \(GLEIF\) database. Validation checks for format validity, MOD 97-10 checksum integrity, GLEIF existence, entity status \(Active\), registration status \(Issued\), and name and country consistency. Validation occurs automatically in three contexts:

-   **Plain-CSV Reporting Package generation**: All LEI codes in the package are validated in a single batch GLEIF API call. A `Level4_LEI_Validation_Report.csv` file is included in the `Consolidated_Reports.zip` attachment on the request record when generation completes. The request record shows a timestamped validation status message. Package generation is never blocked by LEI validation failures.
-   **Microsoft Excel upload**: When uploading Legal entity, Branch, Third party, or Third-party engagement records, all LEI codes are collected, deduplicated, and batch-validated against GLEIF before rows are processed. The **Save rows with LEI GLEIF errors during Excel upload** system property controls whether rows with GLEIF data failures are saved with a warning or blocked. Format and checksum failures always block rows regardless of this property. If the GLEIF API is unavailable, rows are always saved regardless of this property.
-   **UI forms**: When you enter or update an LEI code field on a [Legal entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-legal-entity.md), [Branch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-branch.md), [Third party](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-third-party.md), or [Third-party engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-tp-engagement.md) record, the system validates the LEI against GLEIF and auto-populates the name and country fields. If you then edit the name or country field to a value that no longer matches GLEIF data, an inline warning is displayed. Records can still be saved with mismatched values.

## Procedure

1.  Configure LEI validation system properties to control upload save behavior and API settings.

    1.  Navigate to **All** &gt; **Digital Operational Resilience Management** &gt; **Properties**.

    2.  In the DORA LEI Validation section, review and update the following properties as needed.

<table id="table_lei_properties"><thead><tr><th>

Property

</th><th>

Default

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Save rows with LEI GLEIF errors during Excel upload** \(`sn_dora_accel.lei_save_on_gleif_error`\)

</td><td>

Yes

</td><td>

Controls whether upload rows are saved when GLEIF validation returns a data failure: LEI not found, entity status not Active, or registration status not Issued. Set to **No** to block affected rows and report them as errors in the upload result. Format and checksum failures always block rows regardless of this setting.

</td></tr><tr><td>

**HTTP timeout for GLEIF API calls** \(`sn_dora_accel.gleif_api_timeout`\)

</td><td>

10000 ms

</td><td>

Maximum wait time in milliseconds for a GLEIF API response before the request is treated as unavailable. Valid range: 1000–60000.

</td></tr><tr><td>

**Max LEIs per GLEIF API request** \(`sn_dora_accel.gleif_batch_size`\)

</td><td>

200

</td><td>

Maximum number of LEI codes sent in a single batch GLEIF API call. Valid range: 1–200. Reduce this value if API timeout errors occur frequently.

</td></tr></tbody>
</table>    3.  Select **Save**.

2.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon and navigate to **Digital resilience third-party registers**, then open **Excel download/upload requests** and select the request record.

3.  Review the **Messages** field in the **Result** section for the LEI validation status message.

    If all LEI codes are valid, the message reads: "Level 4 LEI validation completed successfully. \{N\} LEIs validated."

    If any LEI codes have issues, the message reads: "Level 4 LEI validation completed with warnings. \{X\} of \{N\} LEIs has issues." where X is the count of LEIs that returned a Warning, Fail, or N/A result.

4.  If the message indicates issues, download `Consolidated_Reports.zip` from the attachments area of the request record and open `Level4_LEI_Validation_Report.csv`.

    For descriptions of all columns in the report, see [Level 4 LEI Validation Report columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-lei-validation-report.md).

5.  Review the **Validation Result** and **Validation Messages** columns to identify which LEI codes require attention and why.

    -   **Pass**: LEI found in GLEIF, entity status is Active, registration status is Issued. No action required.
    -   **Warning**: LEI found and Active/Issued, but the name or country value in the system does not match GLEIF data. Review the relevant record and update the name or country if required for regulatory accuracy.
    -   **Fail**: LEI format or checksum is invalid, or the LEI is not found in GLEIF, or entity status is not Active, or registration status is not Issued. Correct the LEI code or underlying record data.
    -   **N/A**: The GLEIF API was unavailable, rate-limited, or timed out during validation. No action required for data accuracy; regenerate the package to retry.
6.  Update the affected records in the system and regenerate the Plain-CSV Reporting Package to confirm that issues are resolved.

    For more information on resolving validation issues, see [Validate Register of Information packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-dora.md).


## Result

When all LEI codes pass validation, the Level 4 LEI Validation Report is still included in the `Consolidated_Reports.zip` attachment and the request record message confirms successful validation.

