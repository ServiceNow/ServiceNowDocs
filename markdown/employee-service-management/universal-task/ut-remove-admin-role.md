---
title: Remove the Universal Task admin role from the admin role
description: Remove the sn\_uni\_task.admin role from the admin role so that you can prevent a user with the default admin role from viewing all Universal Task tables.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring your service for Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Remove the Universal Task admin role from the admin role

Remove the sn\_uni\_task.admin role from the admin role so that you can prevent a user with the default admin role from viewing all Universal Task tables.

## Before you begin

Role required: admin

## About this task

By default, a system administrator also contains the sn\_uni\_task.admin role and can access the Universal Task information. To secure your application, remove the sn\_uni\_task.admin from the admin role. By doing so, you prevent the user with a default admin role from viewing all the Universal Task information.

**Note:** Ensure that you have completed setting up Universal Task before removing the sn\_uni\_task.admin role from the admin role.

## Procedure

1.  Log in as admin.

2.  Navigate to **User Administration** &gt; **Roles**.

3.  Select **admin**.

4.  On the **Contains Roles** tab, click **Edit**.

    **Note:** If you do not see the **Edit** button, change the Application scope to `Global`.

5.  From the Contains Roles List column, highlight and move **sn\_uni\_task.admin** to the Collection column.

6.  Click **Save**.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Hide the template bar on the Universal Task form](ut-hide-template-bar.md)

**Next topic:**[Email notification layout for Universal Task notifications](../concept/email-notification-ut.md)

