---
title: Set up your retail support team
description: Set up your retail support team by creating a group then assigning the sn\_retail.support\_agent role to members of that group.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Retail Core, Retail Core, Retail]
---

# Set up your retail support team

Set up your retail support team by creating a group then assigning the sn\_retail.support\_agent role to members of that group.

## Before you begin

Role required: admin

You can assign a role to a group to grant access to applications and modules to group members.

Before assigning the sn\_retail.support\_agent role to a group of users, you must [Create a user group](https://servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/users-and-groups/task/t_CreateAGroup.html) and then [Add users to a group](https://add%20a%20user%20to%20a%20group/).

When you assign roles to groups rather than to individual users, members of the group inherit the role.

When a user switches groups, the new group role is assigned automatically. For information about the Service Mapping roles, see [Control user access to application services](https://servicenow.com/docs/csh?topicname=control-user-access-to-business-services&version=washingtondc&pubname=washingtondc-it-operations-management).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select the group to which you want to assign a role.

3.  In the **Roles** related list, select **Edit**.

4.  Add the `sn_retail.support_agent` role to the group.

5.  Select **Save**.


