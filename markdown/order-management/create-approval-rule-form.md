---
title: Create Approval Rule form
description: Field descriptions for the Create Approval Rule form in Advanced Approval Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Approval Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Create Approval Rule form

Field descriptions for the Create Approval Rule form in Advanced Approval Management.

<table id="table_ahv_gbt_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Functional name of the approver associated with this approval rule, for example, Contract Manager or VP Finance.

</td></tr><tr><td>

Approval trigger condition

</td><td>

Approval condition that triggers this approval rule.

</td></tr><tr><td>

Approval chain

</td><td>

Sequence of approval steps that an approval request must meet before the request is fully approved.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the approval rule is triggered within a set of steps.

</td></tr><tr><td>

Advanced rule

</td><td>

Option, when selected, for entering a script that identifies the functional approver. Only admins can enter an approver using a script.

</td></tr><tr><td>

Description

</td><td>

Brief explanation of the rule. For example the description of the Contract Manager approval rule could be `Reviews contracts and terms`.

</td></tr><tr><td>

Active

</td><td>

Option indicating that the approval rule is in use. To deactivate the approval rule, deselect this option.

</td></tr><tr><td>

Approver type

</td><td>

Type of approver:-   User: Specific approval user who can approve a request, such as Contract Manager.
-   Group: A group that can approve a request, such as the Contracts group.
-   Dynamic: An approver determined by the advanced approval engine when an approval request is submitted, based on relationships, roles, or rules provided in the **Dynamic approver** field.

</td></tr><tr><td>

Dynamic approver

</td><td>

Rule logic that determines the approver dynamically when an approval request is submitted.

</td></tr><tr><td>

Approval criteria

</td><td>

Option that determines how approval requests are handled:-   All: Indicates all designated approvers must approve the request.
-   Anyone: Indicates that only one approver from multiple approvers must approve the request.

</td></tr><tr><td>

Auto escalate

</td><td>

Option that turns on escalations for the approval rule. Escalation is a mechanism for reassigning an approval request to another approver when the original approver hasn't acted on the request within the defined time set in the **Expected days to complete** field.

</td></tr><tr><td>

Expected days to complete

</td><td>

The number of days, hours, minutes, and seconds that defines the total time allotted to approve or reject the request.

</td></tr><tr><td>

Escalation schedule

</td><td>

The escalation schedule to be applied. The default schedule is the Approval Escalation SLA.

</td></tr><tr><td>

Escalation type

</td><td>

Type of approver for the escalation:-   User: Specific approval user who can approve a request, such as Contract Manager.
-   Group: A group that can approve a request, such as the Contracts group.
-   Dynamic: An approver determined by the advanced approval engine when an approval request is submitted, based on relationships, roles, or rules provided in the **Dynamic escalated assignee** field.

</td></tr><tr><td>

Escalated assignee

</td><td>

The approver designated to act on the approval request instead of the original approver.

</td></tr><tr><td>

Dynamic escalated assignee

</td><td>

Rule logic that determines the escalated assignee dynamically when an approval request is submitted.

</td></tr></tbody>
</table>**Parent Topic:**[Advanced Approval Management reference](advanced-approval-management-reference.md)

**Related topics**  


[Create approval rules](../task/create-approval-rules.md)

