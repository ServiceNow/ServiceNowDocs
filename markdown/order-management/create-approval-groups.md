---
title: Define an approval group
description: Define the approval group, such as a contract or finance group, and the associated approval rule that they review during the approval process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Define an approval group

Define the approval group, such as a contract or finance group, and the associated approval rule that they review during the approval process.

## Before you begin

[Define the approval rule](create-approval-rules.md) associated with this approval group.

Groups are set up in the Group \[sys\_user\] table. For more information on creating groups, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAGroup.md).

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin, sn\_adv\_appr\_mgmt.approval\_rule\_writer

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **Approval Groups**.

4.  Select **New**.

5.  In the **Approval rule** field, select the approval rule associated with the approver.

6.  In the **Group** field, select the group who approves the approval step controlled by the selected approval rule.

    **Note:** The members of the group must have the sn\_adv\_appr\_mgmt.approval\_request\_approver role assigned to them.

7.  Select **Save**.


