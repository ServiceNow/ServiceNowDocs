---
title: Exclude access for specific groups in Workforce Optimization for ITSM manager workspace
description: You can remove access to assignment group data and display only the assignment groups that are relevant for the logged-in user in the Workforce Optimization for ITSM manager workspace.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add or remove access to assignment groups in manager workspace, Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Exclude access for specific groups in Workforce Optimization for ITSM manager workspace

You can remove access to assignment group data and display only the assignment groups that are relevant for the logged-in user in the Workforce Optimization for ITSM manager workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace Configuration** &gt; **Group Exclusions**.

2.  On the **Groups not included in WFO** form, select **New**.

3.  In the **Name** field, enter a meaningful name for one or more groups you want to exclude from displaying in the Workforce Optimization for ITSM manager workspace.

4.  Set the filter conditions to exclude the groups.

    For example, if you define a condition as **\[Name\]** **\[does not contain\]****\[Support\]**, then the Workforce Optimization for ITSM manager workspace doesn't display any groups that contain Support in the group name.

    For information on configuring condition builders, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

5.  Select **Submit**.


**Parent Topic:**[Add or remove access to assignment groups in Workforce Optimization for ITSM manager workspace](../concept/specify-access-assignment-group-wfo-itsm.md)

