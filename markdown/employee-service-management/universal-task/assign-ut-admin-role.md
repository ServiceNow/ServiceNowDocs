---
title: Assign Universal Task admin role
description: Assign the sn\_uni\_task.admin role to the application administrators so that they can integrate and configure Universal Task. Roles control access to features, capabilities, and data.
locale: en-US
release: yokohama
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring your service for Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Assign Universal Task admin role

Assign the sn\_uni\_task.admin role to the application administrators so that they can integrate and configure Universal Task. Roles control access to features, capabilities, and data.

## Before you begin

Role required: sn\_uni\_task.admin

## About this task

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

Before you can assign the sn\_uni\_task.admin role to specific users, the logged-in user must also have the sn\_uni\_task.admin role. By default, the admin role contains the sn\_uni\_task.admin role. Administrators can assign the sn\_uni\_task.admin role to other agents who will work on the Universal Task configuration for their respective services.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Open the group that you want to assign the sn\_uni\_task.admin role to.

3.  In the Roles related list, click **Edit**.

4.  In the Collection list, select **sn\_uni\_task.admin**.

5.  Click **Add**.

6.  Click **Save**.

    The **sn\_uni\_task.min\_admin\_count** property in the System Properties \[sys\_properties\] table ensures that a minimum number of scoped administrators are active at any given time for managing the application. For Universal Task, the minimum count of scoped admins is set to two by default. You can modify this property to increase the minimum count.

    **Note:** Ensure that you have at least two agents with the sn\_uni\_task.admin role. If you assign only one agent with the role and that person is deactivated, you no longer will have an agent who can perform the Universal Task admin duties.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Next topic:**[Create UI actions for your service with Universal Task](config-uiactions-for-ut.md)

