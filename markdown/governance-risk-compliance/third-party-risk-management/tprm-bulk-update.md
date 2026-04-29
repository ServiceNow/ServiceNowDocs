---
title: Update existing records in bulk
description: Update existing records in bulk from the Digital resilience third-party registers using Third-party Risk Management.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Update existing records in bulk

Update existing records in bulk from the Digital resilience third-party registers using Third-party Risk Management.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

Only DORA administrators can view the **Upload** option and perform this task.

**Note:** Annual expense data is used during report generation for conversion and aggregation. Confirm that currencies and annual expense fields are accurate to avoid conversion failures or skipped aggregation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Digital resilience third-party registers**.

2.  Select **Excel download/upload requests** and then create an Excel download request by selecting **New**.

3.  On the form, select **Download** as the request type and fill in the remaining fields.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

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

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

    **Note:** Only DORA administrators can view the **Upload** option and perform this task.

10. Select **Save**.

11. Attach the updated template file by selecting **Attach File** and selecting the file from your local hard drive.

12. Select **Upload**.

13. Navigate to the **Result** section of the upload request to view the records that were uploaded successfully and any errors.

    1.  Correct the errors in the Microsoft Excel spreadsheet.

14. Repeat the steps until all errors are resolved and all records are uploaded successfully.

    The updated records are uploaded in bulk from the Digital resilience third-party registers.


