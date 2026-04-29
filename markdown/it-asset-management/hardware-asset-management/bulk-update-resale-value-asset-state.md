---
title: Perform bulk update of resale value for the assets
description: Update the resale values for assets planned for disposal, and indicate that you want to resell them instead of disposing of them, to streamline the asset resale process.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [download disposal assets, bulk update resale value, hardware asset resale]
breadcrumb: [Create a disposal order, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Perform bulk update of resale value for the assets

Update the resale values for assets planned for disposal, and indicate that you want to resell them instead of disposing of them, to streamline the asset resale process.

## Before you begin

Role required: admin

## About this task

Download the list of the planned assets from the Disposal Documentation task and bulk update whether you want to resell or dispose of the assets. For the assets planned for resale, provide the resale value and save it. Import the updated sheet into the Hardware Asset Workspace. After successful import of the resale sheet, on the Disposal Documentation task, in **Planned Asset** tab, the Resold value column data is auto populated. You can proceed with the asset resale for these planned assets.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Disposal orders** tab.

3.  Select the Number link to open the disposal order record that is in the Documentation stage.

    The Disposal order form is displayed.

4.  Select the **Hardware Disposal Tasks** tab.

5.  Select the Number link to open the Disposal Documentation task.

    The Disposal Documentation form is displayed.

6.  Select the **Planned Assets** tab.

7.  Select the **Download disposal assets** button.

    An Excel sheet is downloaded listing the assets planned for disposal.

8.  Open the downloaded Excel sheet.

9.  Update the column values in the downloaded planned assets for disposal Excel sheet and save it.

    1.  In the Substate column, enter **Sold** to resell the asset or **Disposed** to dispose of the asset.

        **Note:** If an invalid value is entered in the Substate column other than **Sold** or **Disposed**, a validation error is triggered when the updated file is imported to the Hardware Asset Workspace.

    2.  In the Resold value column, enter the amount for reselling the asset.

        **Note:**

        -   When the Substate column value **Sold**, the Resold value column can't be empty, and the amount must be a positive value. If the resold amount is negative or the Resold value column is empty, a validation error occurs when the updated file is imported into the Hardware Asset Workspace.
        -   When the Substate column value is **Disposed**, the Resold value column must be empty.
10. Disposal Documentation form, select **Import**.

11. In the Create New Imported Vendor Data form, do the following:

    -   Enter a name for the import vendor data record in the **Name** field,
    -   Select the **Attach File** link to attach the updated planned assets for disposal Excel sheet.
    -   Select the **Save** button.
    The Vendor data import form is displayed. On the **Details** tab, review the import information. Select the **Vendor Data Import Rows** tab to check if any validations were triggered during the import.

    **Note:** The Comment column displays the validations triggered during the import of the updated resell asset record sheet. Make the required changes in the planned assets for disposal Excel sheet, and repeat step 10 to import the updated sheet.

12. Select the **Disposal Documentation** tab to open the Disposal Documentation task.

13. Select the **Planned Assets** tab.

    The Resold value and Substate column value show the updated value.


## What to do next

On the **Planned Asset** tab, select the assets and proceed with resale. For more information about asset resale, see [Resale hardware assets](create-resale-order.md)

**Parent Topic:**[Create a disposal order](create-disposal-order.md)

**Related topics**  


[Resale hardware assets](create-resale-order.md)

[Create a disposal order](create-disposal-order.md)

