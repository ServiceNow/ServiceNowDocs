---
title: Receive an enterprise asset at a stockroom in the Enterprise Asset Workspace
description: Receive a single enterprise asset that has arrived at your stockroom, whether it's part of a workflow or not, in the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Receive an enterprise asset at a stockroom in the Enterprise Asset Workspace

Receive a single enterprise asset that has arrived at your stockroom, whether it's part of a workflow or not, in the Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.asset\_technician or sn\_eam.enterprise\_asset\_manager

## About this task

This task enables you to receive assets in the following scenarios:

-   **Receiving an enterprise asset with an existing record**

    When you’re receiving an enterprise asset from workflows such as a transfer order or Return Merchandise Authorization \(RMA\), where a repaired asset has arrived at your stockroom, the asset record exists in your ServiceNow instance. You can search for the existing asset record using the Asset tag or Serial number and then receive the asset, which automatically closes the receive task of the source workflow.

-   **Receiving a new enterprise asset at your stockroom**

    When you're physically receiving a new enterprise asset at your stockroom, it's likely that the asset record isn't present in your ServiceNow instance. You can receive new assets through workflows like a purchase order, asset refresh, or RMA with a replacement asset. Through this task, you can create an asset record and associate it with the source workflow, which automatically closes the receive task linked to the source workflow.

-   **Receiving an independent enterprise asset**

    You can receive an enterprise asset that isn't part of any workflow and has arrived at your stockroom.


**Important:** You can also receive an hardware asset only if the Hardware Asset Management application is activated.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  Select the stockroom for which you want to receive the hardware asset.

4.  Select **Receive assets**.

5.  Find the enterprise asset that you want to receive.

    1.  In the Receive assets dialog box, enter the Asset tag or Serial number of the asset that you want to receive in the search field.

    2.  Select **Search**.

        -   If the asset record is found, it appears in the Assets list.

            **Note:**

            The following asset details are displayed:

            -   **Display name**
            -   **Model category**
            -   **Asset tag**
            -   **Quantity**
            -   **State**
            -   **Stockroom**
            -   **Location**
        -   If the asset record isn't found, a message appears indicating that the asset isn't found, along with an option to create the asset record.
6.  Receive the enterprise asset in your stockroom.

    -   If the asset record is found in the Assets list, select the asset record and then select **Receive**.
        -   **Result**
            -   The State of the asset changes from **In transit** to **In stock**.
            -   The **Stockroom** field on the asset form is automatically updated with the stockroom at which you received the asset.
            -   The receive task in the source workflow associated with the asset that you received are automatically closed.
    -   If the asset record isn't found, create one to receive.
        1.  Select **Create asset**.
        2.  In the Create asset dialog box, enter the details.

<table id="table_ftz_wcs_pfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Specific product model of the asset.This field is required.

</td></tr><tr><td>

Model Category

</td><td>

Model grouping of the asset.This field is required.

</td></tr><tr><td>

Serial Number

</td><td>

Serial number of the asset.**Note:** Depending on the Model Category that you selected, this field is either required or optional. For instance, Serial number is required for Computer model category.

Unique fields that are required on the asset records are defined by the identification rules on the associated CI classes defined in the Identification and Reconciliation engine \(IRE\). When you create an asset whose model category is linked to a CI class with an identification rule, you should provide details for at least one of the fields, such as Asset tag, Serial number, and MAC address, that uniquely identify the asset.

</td></tr><tr><td>

Asset Tag

</td><td>

Tag to help track the asset.

</td></tr><tr><td>

Mac Address

</td><td>

MAC address of the asset.

</td></tr><tr><td>

Stockroom name

</td><td>

Name of the stockroom that you selected to receive the asset.This field is automatically populated and is read only.

</td></tr><tr><td>

Source type

</td><td>

Source workflow to which the asset that you’re receiving belongs.-   To receive the asset from a purchase order, select **PO**.
-   To receive the asset from the RMA flow, select **Asset RMA**.
-   To receive the asset through asset refresh workflow, select **Refresh**.


</td></tr><tr><td>

Source ticket

</td><td>

Request number of the source workflow that's associated with the asset that you want to receive.-   To receive an asset from a purchase order or asset refresh order, select the associated PO line number.
-   To receive an asset from an RMA order, select the associated RMA line number.
**Note:** Source tickets are displayed based on the model and source type that you selected.

</td></tr></tbody>
</table>            **Important:**

            Providing the Source type and Source ticket details is optional when creating an asset record. However, including these details links the enterprise asset to the source workflow. This link results in the automatic closure of the Receive task in the source workflow when the asset is created. If you don't include these details, the asset record is still created, but you should close the Receive task manually in the source workflow.

            Note the following points before you consider creating an asset record:

            -   If you're receiving an asset from an RMA workflow, you can create an asset record first. Later, you can manually add the details of this asset in the Asset RMA receive task, and then close the task.
            -   If you're receiving an asset from a purchase order, you can create an asset record for the asset you physically received. However, you can't receive the same asset later through the Receive task on the purchase order.
        3.  Select **Create**.
        -   **Result**
            -   An asset record is created with State as **In stock** and Substate as **Available**.
            -   The **Stockroom** field on the asset form is automatically updated with the stockroom at which you received the asset.
            -   The receive task in the source workflow is automatically closed only if you provided the Source type and Source ticket details.

**Parent Topic:**[Manage the receiving of assets at stockrooms in the Enterprise Asset Workspace](../concept/manage-stockroom-receive-eam.md)

