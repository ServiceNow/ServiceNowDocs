---
title: Manage template access
description: Control who has access to templates in App Engine Studio \(AES\) using the app\_template\_admin role. App template admins activate and deactivate templates and grant other users access to share their templates.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Perform configuration tasks, Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Manage template access

Control who has access to templates in App Engine Studio \(AES\) using the app\_template\_admin role. App template admins activate and deactivate templates and grant other users access to share their templates.

## Before you begin

Role required: admin

## About this task

An administrator grants the app\_template\_admin role to users who will manage template activation, deactivation, and sharing. This role should be granted on non-production instances where App Engine Studio users author and use templates.

To create apps and work with templates in AES, users must be an admin or in the App Engine Studio Users group. If they are in the AES User Limited group, they can only edit existing apps, not create new ones.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select the user you want to give the app\_template\_admin role to.

3.  On the Roles related list, select **Edit**.

4.  Move **app\_template\_admin** from the **Collection** list to the **Roles list**.

5.  Select **Save**.


**Parent Topic:**[Perform AES configuration tasks](../reference/aes-config-tasks.md)

