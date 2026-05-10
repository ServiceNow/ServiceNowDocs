---
title: Configure groups
description: Configure user groups for Financial Services Operations applications for assignment of cases and tasks. You can assign roles to groups to provide access to all group members or assign roles to individual users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure groups

Configure user groups for Financial Services Operations applications for assignment of cases and tasks. You can assign roles to groups to provide access to all group members or assign roles to individual users.

## Before you begin

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   For Financial Services Card Operations: sn\_bom\_card.admin and admin
-   For Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   For Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   For Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   For Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin
-   For Financial Services Business Lifecycle: sn\_bom\_clo\_b2b.admin and admin
-   For Financial Services Client Lifecycle: sn\_bom\_clo\_b2c.admin and admin
-   For Financial Services Know Your Customer: sn\_bom\_kyc.admin and admin
-   For Financial Services Treasury Operations: sn\_bom\_treasury.admin and admin
-   Individual Life Claims: sn\_ins\_claim\_indl.admin and admin
-   Insurance claims: sn\_ins\_gen\_claim.admin and admin

## About this task

User groups are used across most processes in the ServiceNow AI Platform for assigning work to teams and requesting approvals.

Any rule that is applied to a group is automatically assigned to group members. For example, roles and assignment rules are automatically assigned to group members.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Create a group or modify an existing group.

    -   To create a group, click **New**.
    -   To configure an existing group, open the group that you want to configure.
3.  On the form, fill in the fields.

    For detailed instructions and field descriptions, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAGroup.md).

4.  Click **Submit** or **Update**.


## What to do next

-   Assign roles to the group. For more information, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

    Configure agent connector and contributor roles for the group, if required.

    **Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../concept/fso-combine-csm-industry-roles.md).

-   Add users to the group.
-   Associate groups with assignment rules.

