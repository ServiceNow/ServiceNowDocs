---
title: Create a Microsoft Excel download request
description: Create a Microsoft Excel download request to download the records from the Digital resilience third-party registers using Third-party Risk Management for auditing purposes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-excel-upload-download-request.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a Microsoft Excel download request

Create a Microsoft Excel download request to download the records from the Digital resilience third-party registers using Third-party Risk Management for auditing purposes.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Use the Excel download/upload requests module in Digital resilience third-party registers to export the records in Microsoft Excel format. The European Union auditors and regulators can download these records for audits, reviews, and appropriate actions.

**Note:** Annual expense data is used during report generation for conversion and aggregation. Confirm that currencies and annual expense fields are accurate to avoid conversion failures or skipped aggregation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Digital resilience third-party registers**.

2.  Select **Excel download/upload requests** and then create an Excel download/upload request by selecting **New**.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-excel-upload-download-req.md).

4.  Select **Save**.

    After saving a download request, you can choose which records you want to download by navigating to its corresponding tab. For example, you would navigate to the **Contracts** tab for a Excel master template download request or the **Assessments** tab for an Assessments download request.

5.  Select the records that you want from the list and perform one of the following steps.

    When you apply a filter to the list and then select All, the download includes only the records that match the filter.

<table id="choicetable_agc_y2k_fdc"><thead><tr><th align="left" id="d285829e165">

Step

</th><th align="left" id="d285829e168">

Description

</th></tr></thead><tbody><tr><td id="d285829e174">

**Export to excel**

</td><td>

To download records related to Assessments, Branches, Contracts, Functions, Legal Entities, Supply Chains, Third Parties, or Third-Party Engagements, select **Export to Info Excel**. The records export as a Microsoft Excel file.

</td></tr><tr><td id="d285829e192">

**Export to info register**

</td><td>

When making a download request for a Excel master template record, select **Export to Info Register** to export contract records you want as an Microsoft Excel file.

</td></tr></tbody>
</table>    For information on Register of information regulatory packages, see [Register of information regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-dora-roi.md), [Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md), [Validation framework for Register of Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-validation-roi.md), and [Validate Register of Information packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-dora.md).

6.  Add the name that you want for the Microsoft Excel file and select **Save**.

    In releases prior to 21.x.x of Digital resilience third-party registers, downloading the contract created a single sheet with all the contract data. Starting with version 21.x.x of Digital resilience third-party registers, generating a contract report mirrors the UI. The report includes entities, third parties, third-party engagements, and specific contract information in the Microsoft Excel sheet.

    It generates a Microsoft Excel sheet that you can submit directly to your regulatory authority. The file strictly adheres to the format of the template issued by the regulatory authority and includes all necessary details for reporting your third-party engagements.

    Starting with version 20.x.x of Digital resilience third-party registers, you can see choice or reference values in the downloaded Microsoft Excel files. For example, Departments can be created in the system as 'Research and Development'. When the functions are downloaded, department values are displayed as options in the Microsoft Excel template for selection. The template includes drop-down lists for departments, business units, and other yes or no questions \(as seen in the Branch template\). Additional drop-downs are added for countries, currencies, etc.

    The application also handles translations for meta data, including headers and drop-down options.

    Verify that no duplicate records are present after downloading data for legal entities, functions, and similar items. The downloaded template contains no duplicate Third-party rows. For example, two DORA entities sharing a vendor and entity produce one Third-party row in the template, not two. You can add new entities and enter their LEI in the downloaded contract file without downloading the contract records again. Upload the modified contract records back to the application.

    **Note:** During Excel upload, duplicate rows in the Contractual Arrangements – Specific Information \(B.02.02\) table are automatically detected and rejected. Rejected rows are logged to the upload error report. During CSV package download, duplicate rows in B.02.02 and in the ICT service supply chains \(B.05.02\) table are flagged in the request record's error log; duplicates are warned but not removed from the generated CSV.

7.  To export Excel download/upload requests, select the requests you want and then **Export**.

<table id="choicetable_zpm_dmr_xcc"><thead><tr><th align="left" id="d285829e328">

Step

</th><th align="left" id="d285829e331">

Description

</th></tr></thead><tbody><tr><td id="d285829e337">

**Select __File Type__.**

</td><td>

File type selected for the export. Available choices are:-   **Excel**
-   **CSV**
-   **JSON**
-   **PDF**


</td></tr><tr><td id="d285829e367">

**Select __Delivery Type__.**

</td><td>

Delivery type selected for the export. Available choices are:-   **Download**
-   **Email**


</td></tr><tr><td id="d285829e389">

**Select __Export.__**

</td><td>

Action to export the record.

</td></tr></tbody>
</table>
