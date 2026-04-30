---
title: Approval rule grouping and sequencing
description: As a Procurement Administrator, you can associate approval rules with approval groups and define the sequence to determine when these rules should be triggered. With this association, a set of approval rules within a rule group is triggered in sequence, instead of all of them being evaluated simultaneously.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create an approval rule, Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval rule grouping and sequencing

As a Procurement Administrator, you can associate approval rules with approval groups and define the sequence to determine when these rules should be triggered. With this association, a set of approval rules within a rule group is triggered in sequence, instead of all of them being evaluated simultaneously.

For example, when purchasing an IT-related product, a manager can first approve the purchase before sending it to the IT department for approval.

Rules within an approval group are evaluated only if all the rules within it are satisfied. If there are multiple approval groups, all groups are evaluated simultaneously. For approval rules that do not have an associated approval group, evaluation is done as-is at the same time with rules that are associated to approval groups. By default, all rules in an approval group are also evaluated independently. If a rule group is satisfied, then the individual rules do not need to be evaluated. This prevents a Procurement Administrator from creating duplicate rules that need to be evaluated independently and also within the context of an approval group.

Consider the following scenarios:

## Scenario 1

-   Purchase requisition amount is $8,000
-   Business owner’s job code is IC3, cost center is Engineering
-   Business owner’s managerial job code hierarchy is IC3 =&gt; M3 =&gt; M4 =&gt; CFO

![Approval rules A and B](../image/approval_rule_grouping_1.png "Approval rules A and B")

-   Without rule group and group sequencing, approval rules A and B are triggered simultaneously.
-   With rule group and group sequencing, approval rule A is triggered first, followed by approval rule B when A is complete.

## Scenario 2

-   Purchase requisition amount is $8,000, supplier product belongs to the XYZ product category
-   Business owner’s job code is IC3, cost center is Engineering
-   Business owner’s managerial job code hierarchy is IC3 =&gt; M3 =&gt; M4 =&gt; CFO

![Approval rules A, B, and C](../image/approval_rule_grouping_2.png "Approval rules A, B, and C")

-   Without rule group and group sequencing, approval rules A, B, and C are triggered simultaneously.
-   With rule group and group sequencing, approval rules A and C are triggered first, followed by approval rule B when A is complete.

## Scenario 3

-   One purchase made for $120k
-   Another purchase made for $95k

![Approval rules A, B, C, and D](../image/approval_rule_grouping_3.png "Approval rules A, B, C, and D")

-   Without rule group and group sequencing, approval rules A, B, C, and D are triggered simultaneously.
-   With rule group and group sequencing, approval rules A and D are triggered first, followed by approval rules B and C when A is complete.

Approval group details are stored in the Approval Group table. Within each approval group, there is an approval rule composition related list to define the order of approval rule evaluation within that specific group.

## Impact of rule groups and sequencing on the resend approval for reassessment property

If approval rules that belong to a rule group are triggered, the resend approval for reassessment property is only applicable if the same rules within that rule group are satisfied as a result of a merge or revision.

In the scenario where there are rules that belong to a group, and are also evaluated independently, the resend approval for reassessment property is only applicable if the same rules within the group are triggered. For rules that do not belong to a group, the property behaves as-is.

For example, in scenario 2:

-   If the resend approval for reassessment property is set to No, and as a result of a revision, approval rule A is satisfied, rule B is not satisfied, and rule C is satisfied, then approvals are resent to the approver for rule A.
-   If the property is set to No, and rules A, B, and C are satisfied as a result of a revision, then the approvals are not resent.
-   If the property is set to Yes, and rules A, B, and C are satisfied as a result of a revision, then all approvals are resent.
-   If the property is set to Yes, and rules A, C, and a new rule D are satisfied as a result of a revision, then approvals A and C are resent, and a new approval D is sent.

**Parent Topic:**[Create an approval rule](../task/create-approval-rule.md)

