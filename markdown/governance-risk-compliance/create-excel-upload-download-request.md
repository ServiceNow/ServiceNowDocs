---
title: Create Microsoft Excel download and upload request
description: Create a Microsoft Excel upload and download request to upload and download the records from and into the Digital resilience third-party registers for auditing purposes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-excel-upload-download-request.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Microsoft Excel download and upload request

Create a Microsoft Excel upload and download request to upload and download the records from and into the Digital resilience third-party registers for auditing purposes.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Use the Excel download/upload requests module in Digital resilience third-party registers to export and import the records in Microsoft Excel format. The European Union auditors and regulators can download these records for audit and reviewing purposes and take appropriate actions.

To become familiar with the process before handling more complex operations, you can follow these steps:

-   Create records on the UI: Create records for each type on the user interface. It helps you to understand which fields are mandatory and their required formats.
-   Download data: Next, download the data to get a clear understanding of the values in each Microsoft Excel column.
-   Upload data with the changes: Finally, make a simple change to a column and upload the data back to verify that the process works as expected.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Select **New**.

    The Create New Excel download/upload request form is displayed.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-excel-upload-download-req.md).

4.  For the Upload request, select the **Attach file** option in the **Select file** field.

5.  To download the template for uploading the selected type of record such as Assessments, select **Download template**, select the file in the **Save as** field in the modal, and select **Save**.

6.  To upload the selected file, select **Upload**.

    During upload, the system performs a two-pass batch LEI verification:

    1.  Collection pass: The system parses the entire Excel file and collects all unique LEI codes from the following fields: - Legal Entity uploads: LEI of the entity \(b\_01\_02\_0010\) - Branch uploads: Identification code of the branch - Third Party uploads: Identification code field \(b\_05\_01\_0010\) where Type of code = LEI - Third-Party Engagement uploads: Identification code field \(b\_05\_01\_0010\) where Type of code = LEI Duplicate LEI codes across multiple rows are deduplicated and verified only once.
    2.  Verification pass: The collected LEI codes are sent to the GLEIF API in a single batch request \(up to 200 LEIs per request\). The results are cached and reused for all rows.
    LEI format validation is always performed locally before the API call. LEIs that do not match the format are reported as errors without calling the GLEIF API.

    The upload result report includes LEI verification messages for each row: - `Success: 'Row {N}: LEI verification successful – LEI {code} – Entity: {name}' - Warning (property = Yes): 'Row {N}: WARNING – LEI verification failed – LEI {code} not found in GLEIF registry. Record saved with unverified LEI.' - Error (property = No): 'Row {N}: LEI verification failed – LEI {code} not found in GLEIF registry. Row skipped'`.

    The behavior for each failure scenario during upload is controlled by the system property **sn\_dora\_accel.lei\_save\_on\_gleif\_error**. For the properties reference and the complete behavior matrix, see [Properties installed with Digital Operational Resilience Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/properties-dora.md).

    During upload of contractual arrangement records, the system checks each row against existing records using the same 8-field duplicate detection logic used on the UI form. Rows that match an existing record are skipped \(not inserted or updated\), and a duplicate error is added to the upload error report.

7.  Select **Save**.

    After saving a download request, you can choose which records you want to download by navigating to its corresponding tab. For example, you would navigate to the **Contracts** tab for a Third-party information register download request or the **Assessments** tab for an Assessments download request.

8.  Select the records that you want from the list and perform one of the following steps.

<table id="choicetable_agc_y2k_fdc"><thead><tr><th align="left" id="d47095e249">

Step

</th><th align="left" id="d47095e252">

Description

</th></tr></thead><tbody><tr><td id="d47095e258">

**Export to excel**

</td><td>

When making a download request for records related to Assessments, Branches, Contracts, Functions, Legal Entities, Supply Chains, Third Parties, or Third-Party Engagements, simply select the **Export to Info Excel** to export those records as a Microsoft Excel file.

</td></tr><tr><td id="d47095e276">

**Export to info register**

</td><td>

When making a download request for a Third-Party Information Register record, select **Export to Info Register** to export contract records you want as an Microsoft Excel file.

 When the export completes, the system runs a batch LEI verification against the GLEIF database for all LEI codes present in the downloaded data. LEIs are processed in batches of 200 per API call. A Level4\_LEI\_Validation\_Report.csv is included in the Consolidated\_Reports.zip file alongside the export data.

 The LEI validation report contains the following columns: "Sheet Name \| Row Number \| LEI Code \| Entity Name \(Input\) \| Country \(Input\) \| LEI Format Valid \| LEI Checksum Valid \| LEI Found \| Name Match \| Name \(GLEIF\) \| Country Match \| Legal Country \(GLEIF\) \| Entity Status \| Registration Status \| Corroboration Level \| Validation Result \| Validation Messages"

 After validation completes, the system displays one of the following messages in the export request record: - Success: 'Level 4 LEI validation completed successfully. \{N\} LEIs validated.' - Warnings present: 'Level 4 LEI validation completed with warnings. \{X\} of \{N\} LEIs has issues.' where X is the count of invalid or unresolvable LEIs.

 LEI validation uses a three-phase pipeline:

-   Phase 1 — Format check: LEIs that fail the 20-character alphanumeric format check are reported immediately and do not proceed to GLEIF.
-   Phase 2 — Checksum check \(MOD 97-10\): LEIs that pass format but fail the ISO 7064 checksum are reported and do not proceed to GLEIF.
-   Phase 3 — GLEIF batch API: Only format- and checksum-valid LEIs are sent to GLEIF. Results are cached in memory for the duration of the download request so that duplicate LEIs are validated only once. If the GLEIF API is unreachable or times out, the download is not blocked; the affected rows are reported as N/A \(API\_UNAVAILABLE\) in the report.
 During CSV generation, the system also checks for duplicate rows in the b\_02.02 sheet \(contractual arrangements\). When rows with an identical composite key \(contract reference, entity, provider, country, function, ICT service type, storage, processing\) are detected, a warning is logged to the DORA request record's error message field indicating the affected row numbers and field values. The duplicate rows are not removed from the generated CSV; they are only warned.

 The following rules apply when the report is generated for b\_05.01 \(ICT third-party service provider\) data:

-   Additional identification code \(c0030\): If a b\_05.01 row's additional identification code is empty or is identical to the primary identification code \(c0010\), it is not validated separately and does not appear as a distinct row in the report.
-   Country comparison for legal entities acting as service providers: When a legal entity that appears in b\_01.02 is also a service provider in b\_05.01, the country in b\_05.01 \(c0080, registered country\) is compared against GLEIF's legal address country to ensure consistent GLEIF country values across both sheets. For third-party-only rows in b\_05.01 \(LEIs not in b\_01.02\), the comparison continues to use the GLEIF headquarters country.


</td></tr></tbody>
</table>    For information on Register of information regulatory packages, see the following topics:

    -   [Register of Information \(ROI\) regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/opres-dora-roi-reg-pkg.md)
    -   [Generate a Register of Information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/opres-drtp-gen-roi-pkg.md)
    -   [Validation framework for Register of Information in Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/opres-dora-validate-roi.md)
    -   [Validate the Register of Information packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/opres-drtp-validate-roi.md)
9.  Add the name that you want for the Microsoft Excel file and select **Save**.

    In releases prior to 21.x.x of Digital resilience third-party registers, downloading the contract created a single sheet with all the contract data. Starting with version 21.x.x of Digital resilience third-party registers, when you generate a report on the contracts, it mirrors the UI and provides details, including information on entities, third parties, third-party engagements, and specific contract information in the Microsoft Excel sheet.

    It generates a Microsoft Excel sheet that you can submit directly to your regulatory authority. The file strictly adheres to the format of the template issued by the regulatory authority and includes all necessary details for reporting your third-party engagements.

    Starting with version 20.x.x of Digital resilience third-party registers, you can see choice or reference values in the downloaded Microsoft Excel files. For example, Departments can be created in the system as 'Research and Development'. When the functions are downloaded, department values are displayed as options in the Microsoft Excel template for selection. The template includes drop-down lists for departments, business units, and other yes or no questions \(as seen in the Branch template\). Additional drop-downs are added for countries, currencies, and so on

    The application also handles translations for meta data, including headers and drop-down options.

    Confirm that no duplicate records are present after downloading data for Legal entities, Functions, and so on. When downloading the template, confirm that there are no duplicate third-party rows. For example, creating one DORA third-party and two DORA entities, then creating DORA contracts for the same vendor using the same entity, results in only one third-party row in the downloaded template and not two duplicate rows. You can add new entities and enter their LEI \(even if not in the drop-down list\) in the downloaded contract file without needing to download the contract records again. You can upload the modified contract records back to the application.

10. Review the LEI validation report, open the "Consolidated\_Reports.zip" that gets generated with the download, locate Level4\_LEI\_Validation\_Report.csv inside, review any LEI codes flagged as invalid or unresolvable, correct the affected records in the system, and re-download if required.

11. Convert and aggregate contractual expenses to regulator-required currencies.

    Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, currency conversion and third-party aggregation capabilities are supported for DORA reporting. For more information on conversion and aggregation, see [Convert and aggregate contractual expenses to regulator-required currencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-excel-report-aggregate-expenses.md).

12. To download third-party information register, select **Export info register** on the Contractual arrangements tab, add a name, and save it.

    The dialog box is shown in the example.

    \[Omitted image "download-register-for-currency.png"\] Alt text: Download third-party information register.

    The example shows a downloaded report with expenses reported in local currencies.

    \[Omitted image "downloaded-report-in-local-currency.png"\] Alt text: Downloaded report with expenses reported in local currencies.

13. To export Excel download/upload requests, select the requests you want and then **Export**.

<table id="choicetable_zpm_dmr_xcc"><thead><tr><th align="left" id="d47095e506">

Step

</th><th align="left" id="d47095e509">

Description

</th></tr></thead><tbody><tr><td id="d47095e515">

**Select __File Type__.**

</td><td>

File type selected for the export. Available choices are:-   **Excel**
-   **CSV**
-   **JSON**
-   **PDF**


</td></tr><tr><td id="d47095e545">

**Select __Delivery Type__.**

</td><td>

Delivery type selected for the export. Available choices are:-   **Download**
-   **Email**


</td></tr><tr><td id="d47095e567">

**Select __Export.__**

</td><td>

Action to export the record.

</td></tr></tbody>
</table>
-   **[Create New Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-excel-upload-download-req.md)**  
On the Create New Excel download/upload request form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

