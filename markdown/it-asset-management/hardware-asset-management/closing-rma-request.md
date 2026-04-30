---
title: Closing an RMA request
description: After you submit an RMA request for a defective asset, you must go through various tasks to finalize repairing or replacing the asset.Close the Assessment task for an RMA request so that the defective assets can get repaired or replaced.Close an RMA request in which a faulty asset is repaired or replaced in the location of the vendor.Close an RMA request in which the faulty assets are repaired on-site.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Manage RMA requests, Use, Hardware Asset Management, IT Asset Management]
---

# Closing an RMA request

After you submit an RMA request for a defective asset, you must go through various tasks to finalize repairing or replacing the asset.

To close an RMA request, you have to close each of its request lines separately. To close a line, you have to complete all of the line's RMA tasks, and you must provide any necessary information about the line. You close a line by first closing its Assessment task. Then the defective asset is sent for either off-site or on-site repair. The line is closed after all these tasks are finished.

The following procedures explain how to close a single line by closing its tasks. You must repeat these procedures for all the request lines.

**Parent Topic:**[Manage RMA requests](manage-rma-req.md)

## Close the Assessment task for an RMA request

Close the Assessment task for an RMA request so that the defective assets can get repaired or replaced.

### Before you begin

Role required: asset, inventory user, or itil

The asset, inventory\_user, or itil role can only access the reports of the RMA request lines.

### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Return Merchandise Authorization** &gt; **All RMA Requests**.

    The RMA Request page appears and shows a list of RMA requests.

2.  Open the RMA request that you want to close.

3.  Under the RMA Request Lines related list, open an RMA request line.

4.  Under the Asset RMA Tasks related list, open the Assessment task.

5.  On the form, fill in the fields.

<table id="table_j4h_1lg_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the task.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom of the faulty asset or consumable.

</td></tr><tr><td>

Vendor

</td><td>

Vendor from which the asset was purchased.

</td></tr><tr><td>

Vendor RMA number

</td><td>

RMA reference number given by your asset vendor.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the RMA task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User from the assignment group to whom the RMA task is assigned.

</td></tr><tr><td>

RMA action

</td><td>

Action to perform on the RMA. The asset can be repaired either on-site or off-site at the vendor's location. Choices are as follows:-   **On-site**
-   **Off-site**
 Before you close the task, you must update this field.

</td></tr></tbody>
</table>6.  Click **Close Task**.

    In the Asset form, the state of the faulty asset changes to In stock and the substate changes to Pending repair.

    If the faulty asset is part of an asset bundle, then after closing the Assessment task, the state of the bundle changes to In stock and Pending repair. If there are multiple RMA requests from a bundle, the state of the bundle remains as In stock, and Pending repair until all the RMA requests are closed.


### Result

Based on whether you selected **On-site** or **Off-site** from the **RMA action** field, either the Asset RMA On-site flow or the Asset RMA Off-site flow is triggered to generate the related RMA tasks to complete the RMA process.

## Close an RMA request with off-site repair or replacement

Close an RMA request in which a faulty asset is repaired or replaced in the location of the vendor.

### Before you begin

Role required: asset, inventory user, or itil

### About this task

After you select **Off-site** from the **RMA action** field on the Assessment task form, a Shipment task is generated under the Asset RMA Tasks related list in the RMA request line. Close the Shipment task and the other RMA tasks one by one to complete the RMA process.

You can cancel an RMA request line that was triggered from an Asset RMA Off-site flow if you have the inventory user or itil role. To cancel an RMA request line, you must do it before the Shipment task is closed.

### Procedure

1.  In the RMA Request Line form, under the Asset RMA Tasks related list, open the Shipment task.

2.  On the form, fill in the fields.

<table id="table_g1d_ffh_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the Shipment task.

</td></tr><tr><td>

Vendor RMA number

</td><td>

RMA reference number given by your asset vendor.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the RMA task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User from the assignment group to whom the RMA task is assigned.

</td></tr><tr><td>

Shipping carrier

</td><td>

Name of the carrier who ships the asset to the location of the vendor for repair or replacement. This field is a reference to the Shipping carrier \[sn\_itam\_shipping\_carrier\] table.

</td></tr><tr><td>

Ship date

</td><td>

Date on which the asset is shipped. To close the task, you have to update this field.

</td></tr><tr><td>

Tracking number

</td><td>

Shipment reference number given by the carrier vendor.

</td></tr></tbody>
</table>3.  Select **Close task**.

    In the Asset form, the state of the asset changes to In transit. In the RMA request line form, under the Asset RMA Tasks related list, a Vendor RMA decision task is generated.

4.  In the RMA request line form, under the Asset RMA Tasks related list, open the Vendor RMA decision task.

5.  On the form, fill in the fields.

<table id="table_fr5_srh_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the Vendor RMA decision task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the RMA task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User from the assignment group to whom the RMA task is assigned.

</td></tr><tr><td>

Vendor action

</td><td>

What the vendor wants to do with the faulty asset. Choices are as follows:-   **Repair**
-   **Replace**
To close the task, you have to update this field.

</td></tr></tbody>
</table>6.  Based on what the vendor wants to do with the faulty asset, do one of the following:

    -   If the vendor wants to repair the faulty asset, select **Repair** from the **Vendor action** field.
    -   If the vendor wants to replace the faulty asset with a new asset, select **Replace** from the **Vendor action** field.
7.  Select **Close task**.

    In the RMA request line form, under the Asset RMA Tasks related list, a Receive task is generated.

8.  In the RMA request line form, under the Asset RMA Tasks related list, open the Receive task.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |State|State of the Receive task.|
    |Assignment group|Group to which the RMA task is assigned.|
    |Assigned to|User from the assignment group to whom the RMA task is assigned.|
    |Asset received|Information on whether you received the repaired or new asset. To close the task, you have to update this field.|
    |Replacement asset|The new asset that you received as a replacement for the faulty asset. This option appears only when **Replace** is selected from the **Vendor action** field in the Vendor RMA decision task.|

10. If you received the repaired asset, do the following:

    1.  From the Asset received list, select **Yes**.

    2.  Select **Close task**.

        In the Asset form, the state of the asset changes to In stock and the substate changes to Available.

11. If you received a new asset as a replacement for the faulty asset, do the following:

    1.  From the Asset received list, select **Yes**.

    2.  Add the new asset to the Asset \[alm\_asset\] table of the Asset form and return back to the Receive task form.

    3.  In the **Replacement asset** field, select the new asset.

    4.  Select **Close task**.

    In the Asset form, the state of the new asset is In stock and the substate is Available. The **Acquisition method** field under the Financial section in the Asset form shows RMA Replacement.

    In the Asset form, the state of the old faulty asset changes to Retired and the substate changes to Vendor credit.

    If a vendor replaces an asset that was part of a bundle with a different model, then a warning appears when you select the new asset. The new model can’t be added to the bundle. If you close the Receive task, the faulty asset is removed from the bundle. The state of the bundle changes to Build, the state of the new asset changes to In stock, and the substate changes to Available.


### Result

The RMA process is complete.

## Close an RMA request with on-site repair

Close an RMA request in which the faulty assets are repaired on-site.

### Before you begin

Role required: asset, inventory user, or itil

### About this task

After you selected **On-site** from the **RMA action** field on the Assessment form, an On-site repair task is generated under the Asset RMA Tasks related list in the RMA request line.

If the asset is successfully repaired on-site, then close the On-site repair task. The RMA process will be complete for the asset that was faulty.

If the asset could not be repaired on-site, you may send the asset for an off-site repair. If you send the faulty asset for an off-site repair, the Asset RMA Off-site flow triggers the required RMA tasks to complete the RMA process.

If you have the inventory user or itil role, then you can cancel an RMA request line that was triggered from an Asset RMA On-site flow until the Repair confirmation task is closed.

### Procedure

1.  In the RMA request line form, under the Asset RMA Tasks related list, open the On-site repair task.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Vendor RMA number|RMA reference number given by your asset vendor.|
    |Assignment group|Group to which the RMA task is assigned.|
    |Assigned to|User from the assignment group to whom the RMA task is assigned.|
    |Repair confirmation|Confirmation on whether the asset was successfully repaired on-site or not. To close the task, you have to update this field.|
    |Action change|Option to send the faulty asset for off-site repair because it couldn't be repaired on-site. This option appears only if you selected **No** from the **Repair confirmation** field.|

3.  If the faulty asset was successfully repaired on-site, then do the following:

    1.  From the Repair confirmation list, select **Yes**.

    2.  Click **Close task**.

    In the Asset form, the state of the asset changes to In stock and the substate changes to Available. The RMA process is complete.

4.  If the faulty asset could not be repaired on-site and you want to send it for an off-site repair, then do the following:

    1.  From the Repair confirmation list, select **No**.

    2.  From the Action change list, select **Off-site**.

    3.  Click **Close task**.

        The Asset RMA Off-site flow is triggered and Shipment task is generated. See [Close an RMA request with off-site repair or replacement](closing-rma-request.md#) for details.

        In the Asset form, the state of the asset changes to In stock and the substate changes to Pending repair.


