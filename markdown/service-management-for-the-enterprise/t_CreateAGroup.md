---
title: Create a group
description: Set up groups and assign the necessary roles and users. The users in the group inherit the roles of the group, so you do not have to assign roles to each user separately.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Create a group

Set up groups and assign the necessary roles and users. The users in the group inherit the roles of the group, so you do not have to assign roles to each user separately.

## Before you begin

Role required: admin

## About this task

There are a few good practices when creating groups:

-   Create one group for administrators and assign the admin role to this group only.
-   Create as many groups as needed in your organization. For example, create a staff group for each geographic location, function, skills, and product models, such as building maintenance or building security. Assign the necessary users to those groups, and then assign the staff role to those groups.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

    See [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for an explanation of each field.

4.  Click the lock icon beside the **Type** field.

    If the field is not visible, configure the form to add it.

    The **Type** field expands.

5.  Click the lookup icon \(![Lookup icon.](../image/SearchIcon.png)\) and select the **\[application\]** type.

6.  Right-click the form header and select **Save**.

7.  Add the \[application\]\_admin or \[application\]\_staff role to the **Roles** related list.

8.  Add users to the **Group Members** related list.

9.  Click **Update**.


**Parent Topic:**[Activate Facilities Service Management](../../facilities-service-management/task/t_ActivateFacilitiesSM.md)

