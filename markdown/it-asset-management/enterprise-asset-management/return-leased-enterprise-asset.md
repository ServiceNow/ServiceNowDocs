---
title: Return a leased enterprise asset
description: Return a leased enterprise asset to the asset vendor before the corresponding lease contract expires.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Managing expiring contracts for leased enterprise assets, Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Return a leased enterprise asset

Return a leased enterprise asset to the asset vendor before the corresponding lease contract expires.

## Before you begin

Before you can proceed with returning a leased enterprise asset, you must complete the Planning task for the associated lease contract. See [Complete the Planning task for an expiring enterprise asset lease contract](complete-leased-asset-planning.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

**Note:** The sn\_eam.enterprise\_asset\_technician role can also perform the Collection, Preparation, and Shipment tasks. However, this role can perform these tasks only through the **Lease-end tasks** Quick links card that is available on the Enterprise asset overview.

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease-end assets** tab, select the lease contract for the enterprise asset that you want to return.

    The lease contract record opens.

3.  Complete and close the Collection task for the lease contract.

    To successfully complete and close this task, you must collect the enterprise asset that you want to return.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Collection** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Collection task opens.

    2.  On the **Details** tab of the Collection task, fill in the fields.

<table id="table_tnk_szj_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Contract Asset Task

</td></tr><tr><td>

Number

</td><td>

Task number that is used to identify and track the Collection task. This field populates automatically.

</td></tr><tr><td>

Contract

</td><td>

Lease contract that the task is associated with. This field populates automatically.

</td></tr><tr><td>

Asset

</td><td>

Enterprise asset that is associated with the lease contract. This field populates automatically.

</td></tr><tr><td>

Location

</td><td>

Current location of the associated enterprise asset. This field populates automatically.

</td></tr><tr><td>

State

</td><td>

State of the task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the task is assigned.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications when work notes are added to the task.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Asset collection

</td></tr><tr><td>

Asset collected

</td><td>

Option that indicates if the associated enterprise asset was collected for return.

 If you select **Yes**, the **Stockroom** field appears next to the **Asset collected** field. In the **Stockroom** field, search for and select the stockroom that the associated enterprise asset was collected from.

 If you select **No**, the **Action change** field appears next to the **Asset collected** field. In the **Action change** field, select an option to change your lease action to either an enterprise asset buyout or lease contract extension.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

        The Collection task automatically closes with an updated state of Closed Complete.

        If you set the **Asset collected** field to **Yes**, the **Substate** field changes to **Pending transfer** in the asset record for the associated enterprise asset.

        If you set the **Asset collected** field to **No**, proceed with one of the following options:

        -   If you changed your lease action to an enterprise asset buyout, proceed to [Buy out a leased enterprise asset](buy-out-leased-enterprise-asset.md).
        -   If you changed your lease action to a lease contract extension, proceed to [Extend the lease contract for an enterprise asset](extend-enterprise-asset-lease-contract.md).
4.  Complete and close the Preparation task for the lease contract.

    To successfully complete and close this task, you must prepare the enterprise asset for return.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Preparation** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Preparation task opens.

    2.  On the **Details** tab of the Preparation task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Contract Asset Task|
        |Number|Task number that is used to identify and track the Preparation task. This field populates automatically.|
        |Contract|Lease contract that the task is associated with. This field populates automatically.|
        |Asset|Enterprise asset that is associated with the lease contract. This field populates automatically.|
        |Location|Current location of the associated enterprise asset. This field populates automatically.|
        |State|State of the task.|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Work notes list|Users who receive notifications when work notes are added to the task.|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Notes|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

        The Preparation task automatically closes with an updated state of Closed Complete.

5.  Complete and close the Shipment task for the lease contract.

    To successfully complete and close this task, you must ship the enterprise asset back to the asset vendor.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Shipment** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Shipment task opens.

    2.  On the **Details** tab of the Shipment task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Contract Asset Task|
        |Number|Task number that is used to identify and track the Shipment task. This field populates automatically.|
        |Contract|Lease contract that the task is associated with. This field populates automatically.|
        |Asset|Enterprise asset that is associated with the lease contract. This field populates automatically.|
        |Location|Current location of the associated enterprise asset. This field populates automatically.|
        |State|State of the task.|
        |Assignment group|Group to which the task is assigned.|
        |Assigned to|User to which the task is assigned.|
        |Work notes list|Users who receive notifications when work notes are added to the task.|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Shipment|
        |Carrier|Shipping carrier through which you shipped the associated enterprise asset.|
        |Ship date|Date on which you shipped the associated enterprise asset.|
        |Tracking number|Tracking number that enables you to track the status and location of the shipment.|
        |Notes|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

        The Shipment task automatically closes with an updated state of Closed Complete.

        In the asset record for the associated enterprise asset, the **State** field changes to **In transit**.

6.  Complete and close the Return confirmation task for the lease contract.

    To successfully complete and close this task, the asset vendor must confirm if they received the enterprise asset that you returned. The asset vendor must also inform you of any settlement payouts that you are receiving for the returned enterprise asset.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Return confirmation** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Return confirmation task opens.

    2.  On the **Details** tab of the Return confirmation task, fill in the fields.

<table id="table_l5z_bfx_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Contract Asset Task

</td></tr><tr><td>

Number

</td><td>

Task number that is used to identify and track the Return confirmation task. This field populates automatically.

</td></tr><tr><td>

Contract

</td><td>

Lease contract that the task is associated with. This field populates automatically.

</td></tr><tr><td>

Asset

</td><td>

Enterprise asset that is associated with the lease contract. This field populates automatically.

</td></tr><tr><td>

Location

</td><td>

Current location of the associated enterprise asset. This field populates automatically.

</td></tr><tr><td>

State

</td><td>

State of the task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the task is assigned.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications when work notes are added to the task.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Return details

</td></tr><tr><td>

Return confirmation

</td><td>

Option that indicates if the associated enterprise asset was returned successfully.To complete the Return confirmation task, you must set this field to **Yes**.

</td></tr><tr><td>

Settlement

</td><td>

Option that indicates if you are receiving a settlement payout for the enterprise asset that you returned.

 If you select **Yes**, the **Settlement amount** field appears below the **Settlement** field. In the **Settlement amount** field, enter the total amount of money that you are receiving from the settlement payout. The Enterprise Asset Management application can then use this information to automatically create a purchase order and purchase order line for the settlement payout.

**Note:** You can set the **Settlement amount** field to any currency of your choice.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

        The Return confirmation task automatically closes with an updated state of Closed Complete.

7.  If you set the **Settlement** field to **Yes** in the Return confirmation task, complete and close the corresponding Return settlement task.

    To successfully complete and close this task, the asset vendor must reimburse you the amount that was specified in the settlement payout.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Return settlement** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Return settlement task opens.

        **Note:** Aside from the **State** field, all editable fields in the Return settlement task are pre-populated based on the corresponding fields that you filled out in the Return confirmation task. The **Purchase order** and **Purchase order line** fields are pre-populated with the purchase order and purchase order line that the Enterprise Asset Management application automatically created for the settlement payout in [step 7](return-leased-enterprise-asset.md#return-confirmation).

    2.  In the Return details section of the **Details** tab, select the Open Record icon \(![Open record icon.](../image/open-record-icon.png)\) in the **Purchase order** field.

        The purchase order record opens.

    3.  Select **Order**.

    4.  After the page reloads, select **Receive**.

        The form closes and you automatically return to the purchase order record, which now has a status of Received.

    5.  Close the purchase order record to return to the Return settlement task.

    6.  Select **Close Task**.

        The Return settlement task automatically closes with an updated state of Closed Complete.


## Result

After you successfully return the leased enterprise asset, the **State** and **Substate** fields change to **Retired** and **Lease Return** in the corresponding asset record.

**Parent Topic:**[Managing expiring contracts for leased enterprise assets](../concept/managing-expiring-contracts-leased-assets.md)

