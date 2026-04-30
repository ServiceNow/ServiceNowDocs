---
title: Close an asset reclamation request
description: Efficiently reclaim hardware assets when an employee leaves an organization or moves to a different role.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reclaim hardware assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Close an asset reclamation request

Efficiently reclaim hardware assets when an employee leaves an organization or moves to a different role.

## Before you begin

Role required: inventory\_user or inventory\_admin

## About this task

For each reclaimed asset, a Hardware Asset Reclamation Line is created. For each Hardware Asset Reclamation Line, at most three Hardware Asset Reclamation Tasks are created.

You must close all the tasks of a Hardware Asset Reclamation Line to close the Hardware Asset Reclamation Line. After all Hardware Asset Reclamation Lines are closed, the Asset Reclamation Request is closed.

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Asset Reclamation** &gt; **Asset Reclamation Request**.

2.  Open the Asset Reclamation Request that you want to close and then open a Hardware Asset Reclamation Line.

    Based the Reclaim method selected while submitting the Asset Reclamation request, a Schedule drop off, Schedule pickup, or Schedule shipment task is created in the Hardware Asset Reclamation Line.

    The **Stage** field of the Hardware Asset Reclamation Line form shows **Ready**.

3.  Open the Schedule drop off, Schedule pickup, or Schedule shipment task that is present in the Hardware Asset Reclamation Line.

4.  On the form, fill in the fields.

<table id="table_pzg_thx_jrb"><thead><tr><th>

Field names

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Group to which the Schedule shipment task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User from the assignment group to whom the Schedule shipment task is assigned.

</td></tr><tr><td>

Stockroom

</td><td>

Location where the reclaimed assets are stored. This field is required.

</td></tr><tr><td>

Shipping carrier

</td><td>

Name of the carrier vendor who ships the asset to the stockroom. This field is required and it is a reference to the Shipment carrier \[sn\_itam\_shipping\_carrier\] table.

</td></tr><tr><td>

Tracking number

</td><td>

Shipment reference number given by the carrier vendor. This field is required.

</td></tr><tr><td>

Ship date

</td><td>

Date on which the asset is shipped. This field is required.

</td></tr><tr><td>

Work notes

</td><td>

Any additional information that you want to mention.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    The **Stage** field of the Hardware Asset Reclamation Line form changes from **Ready** to **Pending received**.

    A Receive asset task is created in the Hardware Asset Reclamation Line.

6.  Open the Receive asset task.

7.  On the form, fill in the fields.

    |Field names|Description|
    |-----------|-----------|
    |Assignment group|Group to which the Receive asset task is assigned.|
    |Assigned to|User from the assignment group to whom the Receive asset task is assigned.|
    |Is asset reclaimed?|Select this check box if you’ve received the assets. This check box is required.|
    |Quantity received|Number of consumables received. This field is required and appears only if the Hardware Asset Reclamation Line is created for a consumable.|
    |Work notes|Any additional information that you want to mention.|

8.  Select **Close Task**.

    The **Stage** field of the Hardware Asset Reclamation Line form changes from **Pending received** to **Pending evaluation**.

    After an asset is received, in the asset form, the following changes occur:

    -   The **Assigned to** field on the asset record becomes empty.
    -   State of the asset changes to In stock and Substate changes to Pending repair.
9.  On the form, fill in the fields.

<table id="table_n1z_4nx_jrb"><thead><tr><th>

Field names

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Group to which the Evaluate asset task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User from the assignment group to whom the Evaluate asset task is assigned.

</td></tr><tr><td>

Evaluation status

</td><td>

Status of the reclaimed asset. This drop-down list is required and the available values are:-   Re-deployable
-   Needs repair
-   To be disposed


</td></tr><tr><td>

Work notes

</td><td>

Any additional information that you want to mention.

</td></tr></tbody>
</table>10. Select **Close Task**.

    Based on what you selected from the **Evaluation status** drop-down list, the State, and Substate of the asset change as follows:

    |Evaluation status values|Asset state and substate|
    |------------------------|------------------------|
    | |State|Substate|
    |Re-deployable|In stock|Available|
    |Needs repair|In stock|Pending repair|
    |To be disposed|In stock|Pending dispose|

    The **Stage** field of the Hardware Asset Reclamation Line form changes from **Pending evaluation** to **Complete**.

    **Note:** When the stage of all Hardware Asset Reclamation Lines has changed to Closed Complete, the state of the Asset Reclamation Request also changes to Complete.


**Parent Topic:**[Reclaim hardware assets](../concept/manage-asset-reclaim.md)

