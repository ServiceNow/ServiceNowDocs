---
title: Verify the display of the right groups in Workforce Optimization for ITSM
description: Verify that the logged in user can access the correct assignment groups data.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add or remove access to assignment groups in manager workspace, Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Verify the display of the right groups in Workforce Optimization for ITSM

Verify that the logged in user can access the correct assignment groups data.

## Before you begin

Role required: sn\_wfo\_cfg\_ws.manager

## Procedure

1.  Impersonate the manager for which you want to verify access.

2.  Select **All** and in the filter navigator, enter `sys_user_grmember.list`.

3.  Select the filter icon and set the condition as **\[Group\]** **\[is\(dynamic\)\]****\[MYWFOGroups\]**.

    The output displays all assignment groups that have access to the manager workspace. This output is based on the configurations in the **Group Exclusions** filter and the implementations using the extension points.

    If the assignment groups listed are missing any groups that the logged-in user must have access to, verify that the **Group Exclusions** filter, and the extension points are configured correctly.


**Parent Topic:**[Add or remove access to assignment groups in Workforce Optimization for ITSM manager workspace](../concept/specify-access-assignment-group-wfo-itsm.md)

