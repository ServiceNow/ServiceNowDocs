---
title: Create Microsoft Excel upload and download request
description: Create a Microsoft Excel upload and download request to upload and download the records from and into the Digital resilience third-party registers for auditing purposes.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Microsoft Excel upload and download request

Create a Microsoft Excel upload and download request to upload and download the records from and into the Digital resilience third-party registers for auditing purposes.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Use the Excel download/upload requests module in Digital resilience third-party registers to export and import the records in Microsoft Excel format. The European Union auditors and regulators can download these records for audit and reviewing purposes and take appropriate actions.

To become familiar with the process before handling more complex operations, you can follow these steps:

-   Create records on the UI: Create new records for each type on the user interface. It helps you to understand which fields are mandatory and their required formats.
-   Download data: Next, download the data to get a clear understanding of the values in each Microsoft Excel column.
-   Upload data with changes: Finally, make a simple change to a column and upload the data back to verify that the process works as expected.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Select **New**.

    The Create New Excel download/upload request form is displayed.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/create-excel-upload-download-req.md).

4.  For the Upload request, select the **Attach file** option in the **Select file** field.

5.  To download the template for uploading the selected type of record such as Assessments, select **Download template**, select the file in the **Save as** field in the modal, and select **Save**.

6.  To upload the selected file, select **Upload**.

7.  Select **Save**.

    After saving a download request, you can choose which records you want to download by navigating to its corresponding tab. For example, you would navigate to the **Contracts** tab for a Third-party information register download request or the **Assessments** tab for an Assessments download request.

8.  Select the records that you want from the list and perform one of the following steps.

<table id="choicetable_agc_y2k_fdc"><thead><tr><th align="left" id="d40312e199">

Step

</th><th align="left" id="d40312e202">

Description

</th></tr></thead><tbody><tr><td id="d40312e208">

**Export to excel**

</td><td>

When making a download request for records related to Assessments, Branches, Contracts, Functions, Legal Entities, Supply Chains, Third Parties, or Third-Party Engagements, simply select the **Export to Info Excel** to export those records as a Microsoft Excel file.

</td></tr><tr><td id="d40312e226">

**Export to info register**

</td><td>

When making a download request for a Third-Party Information Register record, select **Export to Info Register** to export contract records you want as an Microsoft Excel file.

</td></tr></tbody>
</table>    For information on Register of information regulatory packages, see the following topics:

    -   [Register of Information \(ROI\) regulatory packages](../concept/opres-dora-roi-reg-pkg.md)
    -   [Generate a Register of Information package](opres-drtp-gen-roi-pkg.md)
    -   [Validation framework for Register of Information in Operational Resilience](../concept/opres-dora-validate-roi.md)
    -   [Validate the Register of Information packages](opres-drtp-validate-roi.md)
9.  Add the name that you want for the Microsoft Excel file and select **Save**.

    In releases prior to 21.x.x of Digital resilience third-party registers, downloading the contract created a single sheet with all the contract data. Starting with version 21.x.x of Digital resilience third-party registers, when you generate a report on the contracts, it mirrors the UI and provides details, including information on entities, third parties, third-party engagements, and specific contract information in the Microsoft Excel sheet.

    It generates a Microsoft Excel sheet that you can submit directly to your regulatory authority. The file strictly adheres to the format of the template issued by the regulatory authority and includes all necessary details for reporting your third-party engagements.

    Starting with version 20.x.x of Digital resilience third-party registers, you can see choice or reference values in the downloaded Microsoft Excel files. For example, Departments can be created in the system as 'Research and Development'. When the functions are downloaded, department values are displayed as options in the Microsoft Excel template for selection. The template includes drop-down lists for departments, business units, and other yes or no questions \(as seen in the Branch template\). Additional drop-downs are added for countries, currencies, etc.

    The application also handles translations for meta data, including headers and drop-down options.

    Ensure that no duplicate records are present after downloading data for Legal entities, Functions, etc. When downloading the template, ensure that there are no duplicate Third party rows. For example, creating one DORA Third party and two DORA entities, then creating DORA contracts for the same vendor using the same entity, result in only one Third party row in the downloaded template and not two duplicate rows. You can add new entities and enter their LEI \(even if not in the drop-down list\) in the downloaded contract file without needing to download the contract records again. You can upload the modified contract records back to the application.

10. To export Excel download/upload requests, select the requests you want and then **Export**.

<table id="choicetable_zpm_dmr_xcc"><thead><tr><th align="left" id="d40312e356">

Step

</th><th align="left" id="d40312e359">

Description

</th></tr></thead><tbody><tr><td id="d40312e365">

**Select __File Type__.**

</td><td>

File type selected for the export. Available choices are:-   **Excel**
-   **CSV**
-   **JSON**
-   **PDF**


</td></tr><tr><td id="d40312e395">

**Select __Delivery Type__.**

</td><td>

Delivery type selected for the export. Available choices are:-   **Download**
-   **Email**


</td></tr><tr><td id="d40312e417">

**Select __Export.__**

</td><td>

Action to export the record.

</td></tr></tbody>
</table>
-   **[Create New Excel download/upload request form](../reference/create-excel-upload-download-req.md)**  
On the Create New Excel download/upload request form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](../concept/using-dg-registers.md)

