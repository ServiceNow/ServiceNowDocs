---
title: Extend the lease contract for an enterprise asset
description: Extend the lease contract for an enterprise asset before it expires.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Managing expiring contracts for leased enterprise assets, Create and manage contracts for enterprise assets, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Extend the lease contract for an enterprise asset

Extend the lease contract for an enterprise asset before it expires.

## Before you begin

Before you can proceed with extending a lease contract, you must complete the associated Planning task. See [Complete the Planning task for an expiring enterprise asset lease contract](complete-leased-asset-planning.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease-end assets** tab, select the lease contract that you want to extend.

    The lease contract record opens.

3.  Complete and close the Extension task for the lease contract.

    To successfully complete and close this task, you must confirm the lease contract extension details with the asset vendor. These details include the start date, end date, and cost of the lease contract extension.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Extension** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Extension task opens.

    2.  On the **Details** tab of the Extension task, fill in the fields.

<table id="table_tnk_szj_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Contract Asset Task

</td></tr><tr><td>

Number

</td><td>

Task number that is used to identify and track the Extension task. This field populates automatically.

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

Extension details

</td></tr><tr><td>

Extension start date

</td><td>

Date on which you want to start the lease contract extension.

</td></tr><tr><td>

Extension end date

</td><td>

Date on which you want to end the lease contract extension.

</td></tr><tr><td>

Extension cost

</td><td>

Cost to extend the lease contract.**Note:** You can set this field to any currency of your choice.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>    3.  Select **Close Task**.

        The Extension task automatically closes with an updated state of Closed Complete.

4.  Complete and close the Extension confirmation task for the lease contract.

    To successfully complete and close this task, you must pay the asset vendor the amount that was specified in the extension cost.

    1.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Extension confirmation** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

        The Extension confirmation task opens.

        **Note:** Aside from the **State** field and the additional **Extension confirmation** field, all editable fields in the Extension confirmation task are pre-populated based on the corresponding fields that you filled out in the Extension task. The **Purchase order** and **Purchase order line** fields are pre-populated with the purchase order and purchase order line that the Enterprise Asset Management application automatically created for the lease contract extension in the [Planning task](complete-leased-asset-planning.md).

    2.  In the Extension details section of the **Details** tab, set the **Extension confirmation** field to **Yes**.

        This field indicates if the lease contract was extended successfully.

    3.  In the same section, select the Open Record icon \(![Open record icon.](../image/open-record-icon.png)\) in the **Purchase order** field.

        The purchase order record opens.

    4.  Select **Order**.

    5.  After the page reloads, select **Receive**.

        The form closes and you automatically return to the purchase order record, which now has a status of Received.

    6.  Close the purchase order record to return to the Extension confirmation task.

    7.  On the Extension confirmation task, select **Close Task**.

        The Extension confirmation task automatically closes with an updated state of Closed Complete.


## Result

After you successfully extend the lease contract, the **Expiration** field on the lease contract record changes to **Expired**. The Enterprise Asset Management application then creates a new record for the extended lease contract, which is named **EXT\_&lt;_expired-lease-contract_&gt;**. The new lease contract record covers all of the same enterprise assets that were covered in the original lease contract record.

**Parent Topic:**[Managing expiring contracts for leased enterprise assets](../concept/managing-expiring-contracts-leased-assets.md)

