---
title: Set up your retail support team
description: Set up your retail support team by creating a group then assigning the sn\_retail.support\_agent role to members of that group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/retail-operations/rahi-retail-setup-support-team.html
release: australia
product: Retail Operations
classification: retail-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Set up your retail support team

Set up your retail support team by creating a group then assigning the sn\_retail.support\_agent role to members of that group.

## Before you begin

Role required: user\_admin

You can assign a role to a group to grant access to applications and modules to group members.

Before assigning the sn\_retail.support\_agent role to a group of users, you must [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAGroup.md) and then [Add a user to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AddAUserToAGroup.md).

When you assign roles to groups rather than to individual users, members of the group inherit the role.

When a user switches groups, the new group role is assigned automatically. For information about the Service Mapping roles, see [Control user access to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/control-user-access-to-business-services.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select the group to which you want to assign a role.

3.  In the **Roles** related list, select **Edit**.

4.  Add the `sn_retail.support_agent` role to the group.

5.  Select **Save**.


