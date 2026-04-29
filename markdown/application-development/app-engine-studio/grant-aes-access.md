---
title: Grant user access to AES
description: Control who has access to build applications in App Engine Studio \(AES\) by adding users to AES Users group or the AES User Limited group.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Perform configuration tasks, Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Grant user access to AES

Control who has access to build applications in App Engine Studio \(AES\) by adding users to AES Users group or the AES User Limited group.

## Before you begin

Role required: user\_admin or admin

## About this task

Grant access to build applications in AES by adding users to the App Engine Studio Users group in your organization's development instance. Each group member is automatically assigned the sn\_app\_eng\_studio.user role.

To restrict access so that users can work in App Engine Studio but not create apps or see templates, add users to the App Engine Studio User Limited group.

For more information about the differences between the App Engine Studio Users group and the App Engine Studio User Limited group, see [Configure AES personas and roles](../concept/aes-personas-roles.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Add users by selecting either the **App Engine Studio Users** group or the **App Engine Studio User Limited** group.

    1.  In the Group Members related list, select **Edit**.

    2.  On the Edit Members page, move each developer from **Collection** to **Group Members List**.

    3.  Select **Save**.

    4.  On the group record, select **Update**.


**Parent Topic:**[Perform AES configuration tasks](../reference/aes-config-tasks.md)

**Related topics**  


[Components installed with AES](../reference/installed-with-aes.md)

