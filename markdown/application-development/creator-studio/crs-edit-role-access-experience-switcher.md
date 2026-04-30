---
title: Edit a role's access to the experience switcher
description: Add more roles to the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\] to give them access to other products in the experience switcher, such as ServiceNow Studio.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [The experience switcher, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit a role's access to the experience switcher

Add more roles to the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\] to give them access to other products in the experience switcher, such as ServiceNow Studio.

## Before you begin

Role required: admin

## About this task

This topic is for giving non-default roles to the experience switcher. The following roles are already assigned by default:

-   Admins and delegated developers can use the experience switcher because they may need access to any product where they've been delegated to administer or develop an app.
-   Creator Studio users and Creator Studio restricted users don't generally have access to the experience switcher because administrators limit them to a more curated experience.

## Procedure

1.  Navigate to **All** &gt; **sn\_udc\_experience\_visibility\_control.list**.

2.  Select the **New** button.

3.  Enter the experience that you're configuring roles for.

    For example, start typing `cre` to select Creator Studio.

4.  Specify the roles that should get access to the experience.

    1.  Unlock the **Available for roles** field by selecting the lock icon \(![](../image/crs-purple-lock.png)\).

    2.  Start typing and then select the name of the role you're giving access to.

    3.  Lock the **Available for roles** field by selecting the unlock icon \(![](../image/crs-purple-unlock.png)\).

5.  Specify the roles that should not have access to the experience.

    1.  Unlock the **Not available for roles** field by selecting the lock icon \(![](../image/crs-purple-lock.png)\).

    2.  Start typing and then select the name of the role you're restricting access for.

    3.  Lock the **Not available for roles** field by selecting the unlock icon \(![](../image/crs-purple-unlock.png)\).

6.  Select **Submit** to save the changes.


**Parent Topic:**[Administering access to the experience switcher](../concept/crs-experience-switcher-role-access.md)

