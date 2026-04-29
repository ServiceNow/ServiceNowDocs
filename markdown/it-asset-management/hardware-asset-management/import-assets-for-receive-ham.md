---
title: Import and receive assets in bulk at your stockroom in the Hardware Asset Workspace
description: Receive multiple hardware and consumable assets at your stockroom by importing the asset records using an Excel template in the Hardware Asset Workspace.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage the receiving of assets at stockrooms in the Hardware Asset Workspace, Manage stockrooms, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Import and receive assets in bulk at your stockroom in the Hardware Asset Workspace

Receive multiple hardware and consumable assets at your stockroom by importing the asset records using an Excel template in the Hardware Asset Workspace.

## Before you begin

Role required: ham\_admin

## About this task

This task enables you to receive assets with existing records, and also new assets, only if you have provided valid asset details in the template.

When you import a template with asset details, extensive validation is performed on each row. The records from the template and the validation results are stored in the Import asset row \[sn\_itam\_cmn\_import\_asset\_row\] table.

**Note:** The **sn\_itam\_common.receive\_assets\_batch\_size** system property determines how many asset records are processed at once when logging imports and receiving jobs. By default, the system handles 1,000 asset records per batch. With the admin role, you can adjust this number to optimize the system performance and handle large volume of assets. This system property supports domain separation by using the application property.

The asset data validation takes care of the following points:

-   Child assets can't be received.
-   Enterprise assets can only be received if the Enterprise Asset Management application is activated.
-   Operational Technology \(OT\) assets can only be received if the OT Asset Management application is activated.
-   Assets can be received only if the following conditions are fulfilled:
    -   The required fields are provided.
    -   The asset quantity is valid.
    -   The Source type and Source ticket details are valid.
-   Asset from purchase order lines can be received only in Zurich and later releases.
-   Asset bundles can't be received.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select the stockroom for which you want to receive hardware or consumable assets.

4.  Select **Import receiving log**.

5.  Prepare the asset data for import, and then proceed with the import.

    1.  Download, update, and save the asset import template.

        1.  Select **Download Template**.
        2.  Fill in the template with the details of the assets that you want to import and receive.

            The template has the following columns:

            -   **Asset tag** and **Serial number**: These fields are used to determine whether the asset record exists in your ServiceNow instance or not.
            -   **Model category**, **Model name**, and **Model number**: The fields required to validate an asset record depend on the model category. For example, a serial number is required for the Computer model category, and you can receive assets of that model category only if the serial number is provided. Additionally, if an asset record isn't found, fields related to the model are required to create one using the Asset tag and Serial number values provided in the template.
            -   **Quantity**: This field should have a value of 1 for hardware assets, and for consumables, it should reflect the number of assets you’re receiving. You can't receive a partial quantity of consumables.
            -   **Manufacturer**: Asset manufacturer.
            -   **Source type**: The source type is the workflow through which you’re receiving the asset. You should enter values that correspond to the workflows, such as the following:

                -   `TOL` for transfer order line
                -   `POL` for purchase order line
                -   `RMAL` for Return Merchandise Authorization \(RMA\)
                **Note:** This field is required for a consumable asset so that the correct asset is identified and received.

            -   **Source ticket**: The request number of the source workflow that's associated with the asset that you want to receive, such as TO line number, PO line number, or RMA line number.

                **Note:** This field is required for a consumable asset so that the correct asset is identified and received.

            -   **Reserved for**
            -   **Parent asset**
            -   **MAC address** and **OT entity**: These fields are required to identify and receive OT assets.
        3.  Save the template.
    2.  On the Create New Import asset data form, fill in the details.

        1.  In the **Name** field, provide a name for the asset import record.
        2.  Select **Attach file** and then select the asset import template that you created in step a.
    3.  Select **Import**.

        -   The **Import asset data rows** tab is displayed, showing all the asset record rows that were imported through the Excel template.

            **Note:** Depending on the number of records being processed, it might take some time for the asset records to appear in the Import Asset Data Rows tab.

        -   The **Status** column indicates whether the asset is ready to be received. Here are the possible values:
            -   **Ready to receive**: This status indicates that the asset data is valid and ready to be received at your stockroom.
            -   **Receive error** \(Asset not found\): This error indicates that no asset records match the details you provided in the template. However, since the details are valid, asset records will be created when you proceed with the Receive action.
            -   **Import error**: This error is because of the invalid asset data provided in the asset import template, such as duplicate serial numbers or invalid quantity for hardware assets.
        -   The **Alert** column provides details about any errors and the steps that you should take to resolve them and successfully receive the asset.
        **Note:** You can proceed to receive assets with a status of Ready to receive or Receive error.

        For assets with a status of Import error, correct the data issues in your template and create a new import record to import the corrected template. You can then receive the assets.

6.  Receive assets at your stockroom.

    1.  Select the import data rows corresponding to the assets that you want to receive.

    2.  Select **Receive**.

    If you received the assets with Status Ready to receive, the following changes happen:

    -   The State of the assets changes from **In transit** to **In stock**, and the Substate of the assets changes from **Reserved** to **Available**.
    -   The **Stockroom** field on the asset form is automatically updated with the stockroom at which you received the assets.
    -   The receive tasks in the source workflows associated with the assets that you received are automatically closed.
    If you received the assets with Status Receive error, the following changes happen:

    -   Asset records are created with State as **In stock** and Substate as **Available**.
    -   The **Stockroom** field on the asset form is automatically updated with the stockroom at which you received the assets.
    -   The receive task in the source workflow is automatically closed only if you provided the Source type and Source ticket details.

**Parent Topic:**[Manage the receiving of assets at stockrooms in the Hardware Asset Workspace](../concept/manage-stockroom-receive-hws.md)

