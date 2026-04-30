---
title: Assign additional managers to user groups when Workforce Optimization for Field Service is installed
description: When Workforce Optimization for Field Service is active, you can appoint additional managers for your user groups, ensuring the continuity of work in the absence of a manager.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring users, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Assign additional managers to user groups when Workforce Optimization for Field Service is installed

When Workforce Optimization for Field Service is active, you can appoint additional managers for your user groups, ensuring the continuity of work in the absence of a manager.

## Before you begin

Role required: sn\_wfo.admin

## About this task

[Workforce Optimization for Field Service](../concept/configuring-wfo-fsm.md) must be active to add additional managers to user groups.

## Procedure

1.  Navigate to **All** &gt; **Agent Group Management** &gt; **Additional Managers**.

2.  Select **New**.

3.  In the **Assignment Group** field, use the lookup icon to select or create a user group.

    Make sure that the user has the wm\_manager role. For more information on assigning roles to users, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

4.  In the **Manager** field, use the lookup icon to select or create a user.

5.  Select **Submit**.

    You can assign multiple managers to a user group by repeating the steps for each manager.


