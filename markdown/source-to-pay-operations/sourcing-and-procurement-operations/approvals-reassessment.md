---
title: Approvals reassessment
description: Review the conditions for approvals reassessment and their impact on purchase automation.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approvals reassessment

Review the conditions for approvals reassessment and their impact on purchase automation.

## Resend approvals for reassessment property

The sn\_shop.approval.reassessment.resend purchasing property determines if an approval needs to be reassessed as a result of a revision or a merge. The revision could be that of a purchase order or a purchase requisition. This property is only applicable if the same approval rule is triggered. If a new rule is triggered, this property is not applicable and a new approval plan is generated.

For information on approval rule groups and sequencing, and how these impact the property, see [Approval rule grouping and sequencing](approval-rule-sequencing.md).

A reduction in funds revision is not allowed if the amount is below what has already been shipped or delivered. Revisions are not allowed on rejected lines, and therefore reassessment of approvals is not applicable.

For information on approval rules, see [Approval rule types](approval-rule-types.md) and [Create an approval rule](../task/create-approval-rule.md).

When an approval reassessment is sent to approvers, the approval amount to be considered must include the revised line's original amount and the increase in funds. For example, if the original line amount is $1000 and an increase in funds revision results in the line amount to be $1500, the amount to be considered for reassessment and approval is $1500.

When the resend approvals for assessment property is set to Yes, if there is an existing approval plan record that is in progress, and a revision or merge occurs before the plan is completed, its status is updated to No longer required, and a new plan is created. If the property is set to No, and if the existing approval plan is in progress, it is reused.

During an approval reassessment, rejection of a fully received line is not allowed. In Shopping Hub, the fully received line is displayed under the **Approved** tab.

## Population of due date on approvals

When a new approval record is generated and the state of the approval record is Requested, the due date for the record is calculated and populated using the following properties:

-   sn\_shop.pr.approval.duration: Duration, in hours, allocated for an approver to complete the approval request. By default, it is set to 9 hours.
-   sn\_shop.pr.approval.duration.schedule: The type of schedule associated to the approval duration. By default, it is set to 8-5 weekdays, excluding holidays.

    **Note:** The sys\_id of the schedule is used as the value for this property.


Parallel approval records have the same due date. For sequential approvals, the first approver's due date is populated based on the property value defined, the second approver's due date is calculated after the first approval is complete, and so on.

## Creation of breached approvals review task

If a due date for an approval is breached, a new task is automatically created using the \[PSM\] Approval Due Date Breached scheduled job, which runs once a day. This task is a purchasing task, with subtype Approval, and is assigned to the same person to whom the purchase requisition is assigned.

For sequential approval, this purchasing task is created for each approver record that is overdue. For parallel approvals, a single task is created with a related list displaying all the relevant approver records that have breached.

The due date of this task is populated with the breach time on the SLA instance record associated to the SLA definition for the breached approvals review.

For approvals that are no longer required or are canceled, the breached approvals review task creation is not triggered. Breached approvals review SLAs are deleted as they are no longer required.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

