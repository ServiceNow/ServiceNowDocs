---
title: Buy out a leased enterprise asset
description: Buy out a leased enterprise asset before the corresponding lease contract expires.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Managing expiring contracts for leased enterprise assets, Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Buy out a leased enterprise asset

Buy out a leased enterprise asset before the corresponding lease contract expires.

## Before you begin

Before you can proceed with buying out a leased enterprise asset, you must complete the Planning task for the associated lease contract. See [Complete the Planning task for an expiring enterprise asset lease contract](complete-leased-asset-planning.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease-end assets** tab, select the lease contract for the enterprise asset that you want to buy out.

    The lease contract record opens.

3.  Complete and close the Buyout task for the lease contract.

    To successfully complete and close this task, you must confirm a buyout date and amount with the asset vendor.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Buyout** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        ![Current task field.](../image/current-task-lease.png)

        The Buyout task opens.

    2.  On the **Details** tab of the Buyout task, fill in the fields.

<table id="table_tnk_szj_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Contract Asset Task

</td></tr><tr><td>

Number

</td><td>

Task number that is used to identify and track the Buyout task. This field populates automatically.

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

Buyout details

</td></tr><tr><td>

Buyout date

</td><td>

Date on which you are buying out the associated enterprise asset.

</td></tr><tr><td>

Buyout amount

</td><td>

Cost to buy out the associated enterprise asset.**Note:** You can set this field to any currency of your choice.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

        The Buyout task automatically closes with an updated state of Closed Complete.

4.  Complete and close the Buyout confirmation task for the lease contract.

    To successfully complete and close this task, you must pay the asset vendor the confirmed buyout amount on or before the confirmed buyout date.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Buyout confirmation** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        ![Current task field.](../image/current-task-lease.png)

        The Buyout confirmation task opens.

        **Note:** Aside from the **State** field and the additional **Buyout confirmation** field, all editable fields in the Buyout confirmation task are pre-populated based on the corresponding fields that you filled out in the Buyout task. The **Purchase order** and **Purchase order line** fields are pre-populated with the purchase order and purchase order line that the Enterprise Asset Management application automatically created for the enterprise asset buyout in the [Planning task](complete-leased-asset-planning.md).

    2.  In the Buyout details section of the **Details** tab, set the **Buyout confirmation** field to **Yes**.

        This field indicates if you bought out the enterprise asset successfully.

    3.  In the same section, select the Open Record icon \(![Open record icon.](../image/open-record-icon.png)\) in the **Purchase order** field.

        The purchase order record opens.

    4.  Select **Order**.

    5.  After the page reloads, select **Receive**.

        The form closes and you automatically return to the purchase order record, which now has a status of Received.

    6.  Close the purchase order record to return to the Buyout confirmation task.

    7.  On the Buyout confirmation task, select **Close Task**.

        The Buyout confirmation task automatically closes with an updated state of Closed Complete.


## Result

After you successfully buy out the enterprise asset, the **Date removed** field on the lease contract record automatically updates with the date on which you completed all buyout tasks. Following this date, you can no longer track the enterprise asset through this lease contract record.

**Parent Topic:**[Managing expiring contracts for leased enterprise assets](../concept/managing-expiring-contracts-leased-assets.md)

