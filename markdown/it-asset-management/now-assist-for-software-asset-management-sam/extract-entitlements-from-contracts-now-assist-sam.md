---
title: Extract entitlements from software contracts using Now Assist for SAM
description: Reduce manual effort by leveraging generative AI to automatically create entitlements by extracting information from software contracts.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2025-10-24"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Extract entitlements from software contracts using Now Assist for SAM

Reduce manual effort by leveraging generative AI to automatically create entitlements by extracting information from software contracts.

## Before you begin

Role required: sam\_user

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

With the Contract entitlement data extraction skill being activated by default, you can upload software contracts in the Software Asset Workspace to automatically generate entitlements.

You can extract data related to entitlements from an existing or a new contract and only from contracts where the contract model is a software license.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Contracts** &gt; **Software contracts**.

2.  Open an existing software contract that is in an active state and where the contract model is a software license.

    You can also select **New** to create a contract. Only the sam\_admin role can create a contract.

3.  Select **Import contract document**.

4.  Select a publisher from the **Publisher** drop-down.

5.  Select **Add file** to attach a PDF or image of a contract.

    **Note:** The file format should be PDF, JPG, JPEG, or PNG and the file size per attachment shouldn’t exceed 4 MB. The maximum page count is 10 pages for images and 25 pages for PDFs.

6.  Select **Upload**.

7.  Select **Next** to go to the Extract entitlements page.

    A message appears informing you that the extracting process is in progress.

8.  Select **Next** once the extraction process is complete.

    The extract entitlements page opens.

    ![Extract entitlements page](../image/extractentitlements.png)

9.  Select the Open tables down arrow next to **Tables**.

10. Select **Entitlements**.

    Review the generative AI predictions for fields and tables. You can edit any predictions that weren’t captured by DocIntel on this page. You can use DocIntel's Draw mode to move or reorder the columns. You can also make edits directly in the table.

11. Select **Submit** after you have reviewed all the predictions on the page.

    The Confirm field predictions message box opens.

12. Select **Confirm and submit**.

    The status changes from **Review** to **Done**. Every time you make changes and select **Submit**, the data extracted from DocIntel changes.

13. Select **Next** to lock in the data and go to the Review entitlements page.

    ![Review entitlements page](../image/reviewentitlements.png)

    The Review entitlements page opens with the entitlement import error records. For each entitlement extracted from the contract document, an entitlement import record is created. The page also shows the PDF or images you uploaded.

    If you selected a publisher in step 4, the system identifies and displays the best matches according to that publisher.

    You can perform inline editing in the list view for all records that are in the **Needs review** status.

14. Select one of the following options:

    -   **Mark as reviewed** for records that have no errors. Additionally, if a record has errors that you don't want to ignore, open that record, rectify the errors, and then select **Mark as reviewed**. If you select **Mark as reviewed**, the status changes to **Reviewed**.
    -   **Ignore** to ignore the errors for a record. Once you ignore a record, the record becomes read only and the status changes to **Ignored**. You can select **Edit** on the record form to change the status of the record to **Needs review** or **Reviewed**. **Edit** appears only for records that are in the **Ignored** or **Reviewed** status.

        **Note:** If a record is marked as **Ignored**, an entitlement doesn't get created.

15. Select **Submit** after you have reviewed and corrected the errors in all the records.

    The entitlements are successfully created.


**Parent Topic:**[Using generative AI skills in Now Assist for SAM](../concept/using-now-assist-sam.md)

