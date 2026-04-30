---
title: Close an enterprise asset reclamation request
description: Close an asset reclamation request to efficiently reclaim enterprise assets when an employee leaves an organization or moves to a different role.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Close an enterprise asset reclamation request

Close an asset reclamation request to efficiently reclaim enterprise assets when an employee leaves an organization or moves to a different role.

## Before you begin

For each reclaimed asset, an Enterprise Asset Reclamation Line is created. You must close all the tasks of a Enterprise Asset Reclamation Line to close the Enterprise Asset Reclamation Line. Once all Enterprise Asset Reclamation Lines are closed, the Asset Reclamation Request is closed.

Role required: sn\_eam.enterptrise\_asset\_manager or sn\_eam.enterptrise\_asset\_technician

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Reclamation requests**.

2.  In the Asset reclamation requests page, open the request that you want to fulfill and select the Enterprise Asset Reclamation Lines related list.

    Based on what reclaim method the user selected while submitting the asset reclamation request, a **Schedule drop off**, **Schedule pickup**, or **Schedule shipment** task is created in the Enterprise Asset Reclamation Line.

3.  Open the **Schedule drop off**, **Schedule pickup**, or **Schedule shipment** task that is present in the Enterprise Asset Reclamation Line.

4.  On the form, fill in the fields.

    |Field names|Description|
    |-----------|-----------|
    |Number|Number assigned to the task.|
    |Task Name|Name of the task.|
    |Asset|Asset number and short description of the asset.|
    |State|Current state of the task.|
    |Return stockroom|Location where the reclaimed assets will be stored.|
    |Assignment group|Group to which the Schedule shipment task is assigned.|
    |Assigned to|User from the assignment group to whom the Schedule shipment task is assigned.|
    |Quantity received|Number of consumables received.|
    |Short description|Short description of the task.|
    |Description|Detailed description of the task.|
    |Carrier|Name of the carrier vendor who ships the asset to the stockroom. This is a mandatory field.|
    |Tracking number|Shipment reference number given by the carrier vendor. This is a mandatory field.|
    |Ship date|Date on which the asset is shipped. This is a mandatory field.|
    |Work notes|Any additional information that you want to mention.|

5.  Select **Close Task**.

    The **Stage** field of the Enterprise Asset Reclamation Line form changes from **Ready** to **Pending received**.

    A Receive asset task is created in the Enterprise Asset Reclamation Line.

6.  Open the Receive asset task.

7.  On the Receive asset task form, fill in the fields.

    |Field names|Description|
    |-----------|-----------|
    |Number|Number assigned to the task.|
    |Task name|Name of the task.|
    |Asset|Asset number and short description of the asset.|
    |State|Current state of the task.|
    |Return stockroom| |
    |Assignment group|Group to which the Receive asset task is assigned.|
    |Quantity received|Number of consumables received. This field appears only if the Hardware Asset Reclamation Line was created for a consumable, and this is a mandatory field.|
    |Assigned to|User from the assignment group to whom the Receive asset task is assigned.|
    |Short description|Short description of the task.|
    |Description|Detailed description of the task.|
    |Work notes|Any additional information that you want to mention.|

8.  Select **Close Task**.

    The **Stage** field of the Enterprise Asset Reclamation Line form changes from **Pending received** to **Pending evaluation**.

    After an asset is received, in the asset form, the following changes occur:

    -   The **Assigned to** field on the asset record becomes empty.
    -   State of the asset changes to **In stock** and substate changes to**Pending repair**.
9.  Open the Evaluate asset task.

10. On the Evaluate asset task form, fill in the fields.

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

Status of the reclaimed asset. This is a mandatory drop-down list and the values are:-   Re-deployable
-   Needs repair
-   To be disposed


</td></tr><tr><td>

Work notes

</td><td>

Any additional information that you want to mention.

</td></tr></tbody>
</table>11. Select **Close Task**.

    Based on what you selected from the **Evaluation status** drop-down list, the State and Substate of the asset change as follows:

    |Evaluation status values|Asset state|Asset substate|
    |------------------------|-----------|--------------|
    |Re-deployable|In stock|Available|
    |Needs repair|In stock|Pending repair|
    |To be disposed|In stock|Pending dispose|

    The **Stage** field of the Enterprise Asset Reclamation Line form changes from **Pending evaluation** to **Complete**.

    **Note:** When the stage of all Enterprise Asset Reclamation Lines has changed to **Closed Complete**, the state of the Asset Reclamation Request also changes to **Complete**.


**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

