---
title: Create or edit approval levels
description: Define the levels of users and user groups that are going to approve the exception requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-create-or-edit-approval-levels.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Create or edit approval levels

Define the levels of users and user groups that are going to approve the exception requests.

## Before you begin

Role required: sn\_vul\_container.vulnerability\_admin, sn\_vul\_cmn.vulnerability\_admin, sn\_vul.remediation\_owner, sn\_vulc.remediation\_owner, sn\_vul\_container.remediation\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Administration** &gt; **Approval Rules**.

2.  Select **New** to create a rule and provide the necessary details.

3.  Or Select an existing Approval rule from the list view to edit the Approver level.

4.  In the Approver Levels section, select the approver level to edit.

5.  On the form, fill/update the fields as per requirement.

<table id="table_cn3_tmz_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Approval level name.

</td></tr><tr><td>

Required approval

</td><td>

Select how many approvals are required for the selected level:-   One approver required
-   All users must approve


</td></tr><tr><td>

Active

</td><td>

Enabled by default, signifying that the approval level is in use.

</td></tr><tr><td>

Order

</td><td>

Execution order of various configurations within a rule. For example, a configuration with an order entry of 100 runs before a configuration with an order entry of 200.

</td></tr><tr><td>

Approval rule

</td><td>

Contains the table and type details for the approval rule.

</td></tr><tr><td>

Assign using

</td><td>

Select an option from:-   User and user group
-   Approval table field
-   Script


</td></tr><tr><td>

Groups

</td><td>

Approver level group consisting of multiple users. The user must have one of the following roles:-   sn\_vul.exception\_approver: For exception management and exception rules
-   sn\_vul.false\_positive\_approver: For false positive
-   sn\_sec\_exception.approver: For exception rule approvals
-   sn\_vul.unassign\_approver: For unassignment approvals


</td></tr><tr><td>

Users

</td><td>

Edit the users listed in the groups.

</td></tr><tr><td>

Approver table

</td><td>

Select an option from:-   Applies to tables
-   Vulnerability State Change Approval


</td></tr><tr><td>

Approver table field

</td><td>

Select an option from:-   Assigned to
-   Assignment group
-   Closed by
-   Deferred by
-   Opened by
-   Resolved by


</td></tr></tbody>
</table>6.  To save the changes, select **Update**.


## What to do next

**How multi-level approvals behave at runtime**

When an approval rule has multiple levels \(Level 1, Level 2, and so on\), the system routes a submitted request through them in order:

-   **Sequential routing** — the request is sent to Level 1 first. The next level is notified only after Level 1 approves. Each level operates on the same change approval record; the approval history shows every level's decision.
-   **One approver required vs. All users must approve** — within a single level, the **Required approval** setting determines whether any one member's approval clears the level, or whether every member must approve. Rejection by any member at an "all users must approve" level rejects the request immediately.
-   **Rejection escalation** — a rejection at any level closes the request as **Rejected**. The request does *not* roll back to a prior level for re-review. The requester may submit a new request with adjusted justification; the new record's **Resubmission context** is set to After Rejection.
-   **Expiry** — if a level does not act within the approval rule's **Approval expiry** period, the request transitions to **Expired**. The finding reverts to its previous state and the requester is notified.
-   **Empty level guardrail** — if a level has no users or groups assigned at the time a request enters it, the request is automatically rejected. Verify every active level has at least one approver before activating the rule.

