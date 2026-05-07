---
title: Define an approval user
description: Define an approver in Advanced Approval Management and the associated approval rule that they review during the approval process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Define an approval user

Define an approver in Advanced Approval Management and the associated approval rule that they review during the approval process.

## Before you begin

[Create the approval rule](create-approval-rules.md) to be associated with the approver.

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin, sn\_adv\_appr\_mgmt.approval\_rule\_writer

## About this task

An approval user is a [user of your instance](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US) as defined in the User \[sys\_user\] table. An approval user can be a dynamic approver, who can approve requests based on certain conditions that you set. For example, a dynamic user could be a user tied to a particular territory or a manager based on your organization's hierarchy.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **Approval Users**.

4.  Select **New**.

5.  In the **Approval rule** field, select the approval rule associated with the approver user.

6.  In the **User** field, select the user who is the approver for the specified approval rule.

    **Note:** Approval users must have the sn\_adv\_appr\_mgmt.approval\_request\_approver role assigned to them.

7.  Select **Save**.


## What to do next

[Define an approval group](create-approval-groups.md).

