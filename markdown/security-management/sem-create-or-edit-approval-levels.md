---
title: Create or edit approval levels
description: Define the levels of users and user groups that are going to approve the exception requests.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
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


