---
title: Approval rule types
description: Approval rule types determine the methods by which approvals are created during the purchase requisition process.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create an approval rule, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval rule types

Approval rule types determine the methods by which approvals are created during the purchase requisition process.

As a procurement administrator, you can define an approval strategy and create approval rules to approve a purchase internally before it’s converted to a purchase order and sent to a supplier. This is a one-place configuration that can drive any kind of approval process that your organization may need.

You can create these approval rule types that go on to determine the conditions under which approval plans are generated and routed:

<table id="table_rxr_hcz_flb"><thead><tr><th>

Approval rule type

</th><th>

Description

</th><th>

Example Scenario

</th></tr></thead><tbody><tr><td>

Dynamic Users or Groups

</td><td>

Approvals are dynamically created and sent to the specified user or group. Approvals are triggered based on the purchasing user's attributes. The approval routing method is restricted to just sending approvals in parallel.

</td><td>

If approval is required from the purchasing user's cost center manager, then at the time when the purchase requisition is sent to pending approval, the rule looks at the record for the user in the **Business Owner** field, dot-walks to the referenced cost center, and sends an approval to whoever is the referenced user in the **Manager** field on the cost center.

</td></tr><tr><td>

Managerial Job Code Hierarchy

</td><td>

Approvals are triggered based on the purchasing user's job code and manager's job code. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.

</td><td>

If approval is required from all users up to the user with an authorized code, then an approval is sent to all users within a management hierarchy up to the user with an authorized job code for the approved purchasing limit that covers the total amount of the purchase requisition.

 If approval is required from the most junior user with an authorized code, then an approval is sent to the most junior user within a management hierarchy up to the user with an authorized job code for the approved purchasing limit that covers the total amount of the purchase requisition.

</td></tr><tr><td>

Managerial Hierarchy

</td><td>

Approvals are triggered based on the purchasing user's manager's hierarchy. The approval routing method can be parallel or sequential, and the approval decision method can be all approvers or any approver.

</td><td>

If approval is required from all managers in hierarchy, then an approval is sent to all users in the purchasing user's \(business owner\) management hierarchy up to the job code specified, when the approval trigger conditions are met.

 If approval is required from the direct manager alone, then an approval is sent to the user's manager in the purchasing user's \(business owner\) management hierarchy.

 If approval is required from the most senior manager, then an approval is sent to the most senior manager in the purchasing user's \(business owner\) management hierarchy up to the job code specified.

</td></tr><tr><td>

Specified Users or Groups

</td><td>

Approvals are triggered based on the specified users or groups. The approval routing method is restricted to just sending approvals in parallel.

</td><td>

 

</td></tr><tr><td>

Cost Center Managers

</td><td>

Approvals are triggered only for purchase requisitions, from multiple cost center managers.​ The approval routing method is restricted to just sending approvals in parallel.

</td><td>

If the cost of a purchase requisition is allocated across many cost centers, approvals are sent to each cost center manager for the cost allocation amount needing approval.

 If an individual item in the purchase requisition has cost allocated across multiple cost centers, all the cost center managers must provide their approval for the amount of that item to be approved.​ The purchase requisition can be partially or completely approved depending on the approval decision for each individual item or purchase line.

 Cost center managers receive email notifications for their approval with details of the purchase and the allocated amount needing approval. They can provide their approval directly from the email, or​ complete their approval in Shopping Hub, Employee Center, Virtual Agent, or Shopping Hub Mobile.

</td></tr></tbody>
</table>## Self-approved purchases

For requesters who possess the right purchasing authority, job code, or belong to designations that meet a defined purchasing approval matrix, their purchases are self-approved. An audit trail is made available, where an approval plan is created with the approval type as Self Approved, and in the Closed Complete state, though no actual approval tasks are created.

Such requesters can also complete approval tasks, if configured, and provide approvals for invoices from suppliers to be routed for payment. In the Approval Rules form, an admin can configure the need for a requester to provide an explicit approval decision, through the **Allow automatic approval** flag. By default, this flag is checked or set to true, enabling the self-approval functionality, where the requester has the approving authority. However, if the flag is cleared or set to false, the requester is included to be an active approver in the approval engine’s generated approval list, thus overriding the default self-approval functionality. The requester now must provide an explicit approval decision by completing an approval task.

**Note:** In case of any issues related to approvals not getting created as expected, ensure that the flag on the rule is in the correct state and the rule conditions are met.

**Parent Topic:**[Create an approval rule](../task/create-approval-rule.md)

