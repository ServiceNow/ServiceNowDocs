---
title: Complete the Planning task for an expiring enterprise asset lease contract
description: Complete the Planning task for an expiring enterprise asset lease contract so that you can proceed with either returning the associated enterprise asset, buying out the associated enterprise asset, or extending the lease contract.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing expiring contracts for leased enterprise assets, Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Complete the Planning task for an expiring enterprise asset lease contract

Complete the Planning task for an expiring enterprise asset lease contract so that you can proceed with either returning the associated enterprise asset, buying out the associated enterprise asset, or extending the lease contract.

## Before you begin

To generate the Planning task for an expiring lease contract, you must initiate the lease-end process for that contract. See [Begin the lease-end process for an expiring enterprise asset lease contract](begin-lease-end-process-eam.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease-end assets** tab, select the lease contract for the enterprise asset that you want to return, buy out, or extend the contract for.

    **Note:** You must select a lease contract that is in the **Planning** stage.

    The lease contract record opens.

3.  On the **Contract Asset Tasks** tab of the lease contract record, select the task number for the **Planning** task.

    Alternatively, select the task number that is displayed in the **Current task** field of the lease contract record header.

    The Planning task opens.

4.  On the **Details** tab of the Planning task, fill in the fields.

<table id="table_tnk_szj_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Contract Asset Task

</td></tr><tr><td>

Number

</td><td>

Task number used to identify and track the Planning task. This field populates automatically.

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

Lease action

</td><td>

Action that you want to take on the associated enterprise asset. Select one of the following options:-   **Return**
-   **Extend**

**Note:** If you select this option, the Enterprise Asset Management application automatically creates a purchase order and purchase order line for the lease contract extension.

-   **Buyout**

**Note:** If you select this option, the Enterprise Asset Management application automatically creates a purchase order and purchase order line for the enterprise asset buyout.

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

Notes

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.


## Result

The Planning task automatically closes with an updated state of Closed Complete.

## What to do next

Based on the action that you selected in the **Lease action** field, complete all necessary tasks to return the associated enterprise asset, buy out the associated enterprise asset, or extend the lease contract.

**Parent Topic:**[Managing expiring contracts for leased enterprise assets](../concept/managing-expiring-contracts-leased-assets.md)

