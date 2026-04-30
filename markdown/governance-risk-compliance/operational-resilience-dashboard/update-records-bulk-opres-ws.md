---
title: Update existing records in bulk
description: Update existing records in bulk from the Digital resilience third-party registers using Third-party Risk Management.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Update existing records in bulk

Update existing records in bulk from the Digital resilience third-party registers using Third-party Risk Management.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

To achieve the best results, upload the records in the following order due to their interdependent reference fields:

1.  Legal Entities
2.  Branches
3.  Functions
4.  Third-parties
5.  Third-party engagements
6.  Contracts
7.  Supply chains
8.  Assessments

Complete the following steps for each data type of the record:

-   Create at least one record on the UI.
-   Create a Download request and select this record to download.
-   Make changes to one or more columns in the downloaded file.
-   Create an Upload request, attach the modified file, and click **Upload**.
-   Verify the changes on the UI for this record.

Repeat these steps for each data type to ensure consistency across all categories. Following this sequence helps ensure data consistency and accuracy across related records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Create an Excel download request by selecting **New**.

3.  On the form, select **Download** as the request type and fill in the remaining fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../../grc-vendor-risk/reference/tprm-excel-upload-download-req.md).

4.  Select **Save**.

    After saving a download request, you can choose which records you want to download by navigating to its corresponding tab. For example, you would navigate to the **Contracts** tab for a Third-party information register download request or the **Assessments** tab for an Assessments download request.

5.  Select the records that you want to update from the list and select **Export to Excel**.

6.  Add the name that you want for the Microsoft Excel file and select **Save**.

    It creates a Microsoft Excel sheet that you can use to make bulk updates for the records you selected.

    After downloading the templates to add options on the reference fields, the upload templates are updated to a dynamic format with drop-downs for choice and reference fields, rather than hard-coding the values.

    The dynamic templates automatically handle translations for headers and reference field options. They fetch these elements in real-time, ensuring they remain up-to-date without the need for manual updates. The default template stays up-to-date because the options are generated dynamically.

    You can view instructions for filling out the template by navigating to the **Instructions** tab of the template file. You can add your updated record creation information by navigating to the **Digital resilience information** tab and filling out the template.

    **Note:** You can only upload or download one type of record for each request. For example, if you made an upload request for Assessment records, you can only include Assessment record information in the template.

7.  Follow the instructions in the template file and add your updated information.

8.  Create an upload request by navigating to **Excel download/upload requests** and selecting **New**.

9.  On the form, select **Upload** as the request type and fill in the remaining fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../../grc-vendor-risk/reference/tprm-excel-upload-download-req.md).

    **Note:** Only DORA administrators can view the **Upload** option and perform this task.

10. Select **Save**.

11. Attach the updated template file by selecting **Attach File** and selecting the file from your local hard drive.

12. Select **Upload**.

13. Navigate to the **Result** section of the upload request to view the records that were uploaded successfully and any errors.

    1.  Correct the errors in the Microsoft Excel spreadsheet.

    2.  Upload the record again.

14. Repeat the steps until all errors are resolved and all records are uploaded successfully.

    The updated records are uploaded in bulk from the Digital resilience third-party registers.


**Parent Topic:**[Using Digital resilience third-party registers](../concept/using-dg-registers.md)

