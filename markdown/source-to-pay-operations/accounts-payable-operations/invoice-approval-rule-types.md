---
title: Approval rule types
description: Approval rule types determine how approvals are created and routed during the invoice approval process.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an approval rule, Invoice approvals, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Approval rule types

Approval rule types determine how approvals are created and routed during the invoice approval process.

The approval rule types determine the conditions under which approval plans are created and routed.

<table id="table_l5g_fn5_4wb"><thead><tr><th>

Approval rule type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Center Managers

</td><td>

Approvals are created and sent to cost center managers. The approval routing method is restricted to just sending approvals in parallel to cost center owners associated with the cost allocation records.**Note:** Invoice cost center managers must have \[sn\_shop\_invoice\_owner\] to view the approval rules for cost allocation.

</td></tr><tr><td>

Dynamic Users or Groups

</td><td>

Approvals are dynamically created and sent to the specified user or group. Approvals are triggered based on the purchasing user's attributes. The approval routing method is restricted to just sending approvals in parallel. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.

</td></tr><tr><td>

Managerial Job Code Hierarchy

</td><td>

Approvals are triggered based on the purchasing user's job code and manager's job code. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.

</td></tr><tr><td>

Managerial Hierarchy

</td><td>

Approvals are triggered based on the purchasing user's manager's hierarchy. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.

</td></tr><tr><td>

Specified Users or Groups

</td><td>

Approvals are triggered based on the specified users or groups. The approval routing method is restricted to just sending approvals in parallel.

</td></tr></tbody>
</table>**Parent Topic:**[Create an approval rule](../task/invoice-approval-rule.md)

