---
title: Configure non-default access to the experience switcher
description: Control which roles have access to the experience switcher in ServiceNow Studio. The experience switcher enables you to easily switch between development environments to use the right tool for your task.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing access to the experience switcher, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Configure non-default access to the experience switcher

Control which roles have access to the experience switcher in ServiceNow Studio. The experience switcher enables you to easily switch between development environments to use the right tool for your task.

## Before you begin

Role required: admin

## About this task

By default, the Experience Configurations table \[sn\_udc\_experience\_configuration\] gives admins and delegated developers access to see the experience switcher. However, you can add non-default roles to the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\] to give access to the experience switcher. For more information about the default roles, see [Working with roles and access in app development tools](../concept/working-with-roles-and-access.md).

-   Admins and delegated developers can use the experience switcher because they may need access to any product where they've been delegated to administer or develop an app.
-   Creator Studio users and Creator Studio restricted users don't generally have access to the experience switcher because administrators limit them to a more curated experience.

## Procedure

1.  Navigate to **All** &gt; **sn\_udc\_experience\_visibility\_control.list**.

2.  Select **New**.

3.  Enter the experience that you're configuring roles for.

    For example, start typing `Serv` to select ServiceNow Studio.

4.  Specify the roles that should get access to the experience.

    1.  Unlock the **Available for roles** field by selecting the lock icon ![](../../creator-studio/image/crs-purple-lock.png).

    2.  Start typing and then select the name of the role you're giving access to.

    3.  Lock the **Available for roles** field by selecting the unlock icon ![](../../creator-studio/image/crs-purple-unlock.png).

5.  Specify the roles that should not have access to the experience.

    1.  Unlock the **Not available for roles** field by selecting the lock icon ![](../../creator-studio/image/crs-purple-lock.png).

    2.  Start typing and then select the name of the role you're restricting access for.

    3.  Lock the **Not available for roles** field by selecting the unlock icon ![](../../creator-studio/image/crs-purple-unlock.png).

6.  Select **Submit**.


**Parent Topic:**[Managing access to the experience switcher](../concept/managing-access-experience-switcher.md)

