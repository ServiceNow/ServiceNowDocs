---
title: Milestones
description: Milestones represent an acknowledgment that a certain deliverable is achieved for a service. You can create a milestone against the purchase line and purchase order line for a service product type, when the acknowledgment type is set to Milestones.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Purchase lines, Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Milestones

Milestones represent an acknowledgment that a certain deliverable is achieved for a service. You can create a milestone against the purchase line and purchase order line for a service product type, when the acknowledgment type is set to **Milestones**.

The key fields of a milestone are:

<table id="table_okp_d1p_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deliverable Name

</td><td>

Name of the milestone

</td></tr><tr><td>

Number

</td><td>

System-generated unique identifier of the milestone.

</td></tr><tr><td>

Assigned to

</td><td>

User primarily responsible for confirming the completion of this milestone.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team who can be contacted with questions about receipts, milestones, invoices, or other activities related to acknowledgment. This field is populated or updated with the same user in the **Assigned to** field of the parent task record, as follows: For a milestone or acknowledgment task, from the referenced purchase order.

</td></tr><tr><td>

Purchase line

</td><td>

Purchase line associated with the milestone.

</td></tr><tr><td>

Purchase order line

</td><td>

Purchase order line associated with the milestone.

</td></tr><tr><td>

State

</td><td>

Status of the milestone.

</td></tr><tr><td>

Due date

</td><td>

Expected completion date from the user this milestone is assigned to.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Completion date

</td><td>

Scheduled completion date for the milestone.

</td></tr><tr><td>

Payout type

</td><td>

The type of the payout associated with this milestone. For example, **Percentage** or **Amount**.

</td></tr><tr><td>

Payout amount

</td><td>

Amount associated with this milestone.This field is displayed if the payout type is set to **Amount**.

 Sum of the amount across all milestones can’t exceed the total amount on the purchase requisition.

</td></tr><tr><td>

Payout percentage

</td><td>

Percentage of the payout amount associated with this milestone.This field is displayed if the payout type is set to **Percentage**.

 Sum of the percentages across all milestones can’t exceed 100%.

</td></tr><tr><td>

Cancellation reason

</td><td>

Reason for the cancellation of the milestone.This field is required when the recipient cancels the milestone.

</td></tr><tr><td>

Deferral reason

</td><td>

Reason for the deferral of the delivery date of the milestone.

</td></tr></tbody>
</table>Milestones are assigned to the recipient of the purchase line. A recipient can either confirm, cancel, or defer milestones using **Confirm completion**, **Cancel**, or **Defer Completion** options.

-   Confirming a milestone updates the state to **Closed Complete**.
-   Canceling a milestone requires a cancellation reason.
-   Deferring the completion of a milestone requires a completion date and the state is updated to **Pending Completion Date**.

When the status of a milestone task is **Closed Complete**, a receipt is created and the **Amount received** or **Percentage received** fields are populated accordingly on the receipt. The receipt triggers the update of the states on the purchase order line and purchase order similar to the workflow of a good receipt.

The \[PSM\] Monitor Milestone Tasks scheduled job monitors the completion date of each active milestone on a daily basis. On the specified date of completion, the job updates the state of the milestone from **Pending Completion Date** to **Confirmation Required**.

The UI action to confirm or defer the milestone is displayed when the state of the milestone is **Confirmation Required**.

**Parent Topic:**[Purchase lines](purchase-lines.md)

