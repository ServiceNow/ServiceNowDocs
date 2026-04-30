---
title: Create a Microsoft Excel download request
description: Create a Microsoft Excel download request to download the records from the Digital resilience third-party registers using Third-party Risk Management for auditing purposes.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
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

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Digital resilience third-party registers**.

2.  Select **Excel download/upload requests** and then create an Excel download/upload request by selecting **New**.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

4.  Select **Save**.

    After saving a download request, you can choose which records you want to download by navigating to its corresponding tab. For example, you would navigate to the **Contracts** tab for a Excel master template download request or the **Assessments** tab for an Assessments download request.

5.  Select the records that you want from the list and perform one of the following steps.

<table id="choicetable_agc_y2k_fdc"><thead><tr><th align="left" id="d111601e159">

Step

</th><th align="left" id="d111601e162">

Description

</th></tr></thead><tbody><tr><td id="d111601e168">

**Export to excel**

</td><td>

When making a download request for records related to Assessments, Branches, Contracts, Functions, Legal Entities, Supply Chains, Third Parties, or Third-Party Engagements, simply select the **Export to Info Excel** to export those records as a Microsoft Excel file.

</td></tr><tr><td id="d111601e186">

**Export to info register**

</td><td>

When making a download request for a Excel master template record, select **Export to Info Register** to export contract records you want as an Microsoft Excel file.

</td></tr></tbody>
</table>    For information on Register of information regulatory packages, see [Register of information regulatory packages](../concept/tprm-dora-roi.md), [Generate a register of information package](tprm-drtp-roi-packages.md), [Validation framework for Register of Information](../concept/tprm-validation-roi.md), and [Validate Register of Information packages](tprm-valid-dora.md).

6.  Add the name that you want for the Microsoft Excel file and select **Save**.

    In releases prior to 21.x.x of Digital resilience third-party registers, downloading the contract created a single sheet with all the contract data. Starting with version 21.x.x of Digital resilience third-party registers, when you generate a report on the contracts, it mirrors the UI and provides details, including information on entities, third parties, third-party engagements, and specific contract information in the Microsoft Excel sheet.

    It generates a Microsoft Excel sheet that you can submit directly to your regulatory authority. The file strictly adheres to the format of the template issued by the regulatory authority and includes all necessary details for reporting your third-party engagements.

    Starting with version 20.x.x of Digital resilience third-party registers, you can see choice or reference values in the downloaded Microsoft Excel files. For example, Departments can be created in the system as 'Research and Development'. When the functions are downloaded, department values are displayed as options in the Microsoft Excel template for selection. The template includes drop-down lists for departments, business units, and other yes or no questions \(as seen in the Branch template\). Additional drop-downs are added for countries, currencies, etc.

    The application also handles translations for meta data, including headers and drop-down options.

    Ensure that no duplicate records are present after downloading data for Legal entities, Functions, etc. When downloading the template, ensure that there are no duplicate Third party rows. For example, creating one DORA Third party and two DORA entities, then creating DORA contracts for the same vendor using the same entity, result in only one Third party row in the downloaded template and not two duplicate rows. You can add new entities and enter their LEI \(even if not in the drop-down list\) in the downloaded contract file without needing to download the contract records again. You can upload the modified contract records back to the application.

7.  To export Excel download/upload requests, select the requests you want and then **Export**.

<table id="choicetable_zpm_dmr_xcc"><thead><tr><th align="left" id="d111601e318">

Step

</th><th align="left" id="d111601e321">

Description

</th></tr></thead><tbody><tr><td id="d111601e327">

**Select __File Type__.**

</td><td>

File type selected for the export. Available choices are:-   **Excel**
-   **CSV**
-   **JSON**
-   **PDF**


</td></tr><tr><td id="d111601e357">

**Select __Delivery Type__.**

</td><td>

Delivery type selected for the export. Available choices are:-   **Download**
-   **Email**


</td></tr><tr><td id="d111601e379">

**Select __Export.__**

</td><td>

Action to export the record.

</td></tr></tbody>
</table>
