---
title: Create approval levels for Exception Management in Configuration Compliance
description: Define the levels of users and user groups that are going to approve the exception requests.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure exception approvals, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create approval levels for Exception Management in Configuration Compliance

Define the levels of users and user groups that are going to approve the exception requests.

## Before you begin

Role required: sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Approval Rules**.

2.  Select an approval rule and navigate to the **Approval Configurations** tab.

3.  Select a configuration.

4.  In the **Approver Levels** section, select an approver level.

5.  On the form, fill in the fields.

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

Contains the table and type details for the approval rule. This field is read-only.

</td></tr><tr><td>

Approval configuration

</td><td>

Contains the approval configurations. This field is read-only.

</td></tr><tr><td>

Assign using

</td><td>

Select an option from:-   User and user group
-   Approval table field
-   Script


</td></tr><tr><td>

Groups

</td><td>

Approver level group consisting of multiple users. The user must have one of the following roles for exception management and exception rules:-   sn\_vulc.exception\_approver
-   sn\_vulc.read
-   sn\_vulc.read\_auto\_exception\_rule


</td></tr><tr><td>

Users

</td><td>

Edit the users listed in the groups.

</td></tr></tbody>
</table>6.  To save the changes, select **Update**.

    **Note:** Prior to v13.0, the workflow process is functional if there are users only in Exception level 1. However, starting from v13.0, there must be at least one user in each level.

    Prior to v13.0, in the workflow, if there was no user in the second level, the remediation task was deferred. However, v13.0 onwards, if there is no user in the second level, the approval request is automatically rejected.


## Example

There can be different approval levels for remediation tasks for Linux and Windows servers.

