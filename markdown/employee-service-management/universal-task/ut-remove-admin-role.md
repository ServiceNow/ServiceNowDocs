---
title: Remove the Universal Task admin role from the admin role
description: After system configuration, remove the Universal Task Admin role \(sn\_uni\_task.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive information via forms, lists and UI.
locale: en-US
release: yokohama
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring your service for Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Remove the Universal Task admin role from the admin role

After system configuration, remove the Universal Task Admin role \(sn\_uni\_task.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive information via forms, lists and UI.

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

