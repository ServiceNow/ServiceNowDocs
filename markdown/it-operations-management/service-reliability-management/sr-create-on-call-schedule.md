---
title: Create an SRM on-call schedule
description: Set up an on-call schedule to make sure that someone is available to respond to incidents and critical alerts.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Create an SRM on-call schedule

Set up an on-call schedule to make sure that someone is available to respond to incidents and critical alerts.

## Before you begin

Before creating an on-call schedule, a team must exist in Service Reliability Management \(SRM\). The Alert table \[em\_alert\] must also be added to the Trigger Rule Table Config list. See [Add an SRM team](sr-create-team.md) and [Add alert table to enable on-call scheduling for Service Operations Workspace for ITOM](../../service-operations-workspace-itom/task/add-alert-table-oncall.md) for more information.

Role required: srm\_manager, srm\_responder, or srm\_admin

## About this task

Shifts in SRM let you define variable time periods for your shift-based workforce. Create shifts for particular dates and times when you need coverage, and assign them to team members.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** &gt; **Teams \(![Teams icon](../image/icon-sr-teams.png)\)**.

2.  On the Teams page, select your team.

3.  Select the **Schedule** tab and then select **Create shift**.

4.  In the Create new dialog, select either **Create new** or **Use template**.

    Your system admin can create predefined templates for you to use to create shifts.

5.  Fill in the fields.

    For more information on the field descriptions, see [Create a shift form in Service Reliability Management](../reference/sr-create-shift-form.md).

6.  Select **Create shift**.


-   **[Set on-call team preferences in SRM](sr-set-on-call-prefs.md)**  
Set on-call preferences for team members to increase the efficiency of your business operations.

**Parent Topic:**[Working with SRM teams](../concept/sr-work-teams.md)

