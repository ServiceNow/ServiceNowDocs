---
title: Define a production day
description: Define a production day for your organization within Industrial Connected Workforce.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prerequisites, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Define a production day

Define a production day for your organization within Industrial Connected Workforce.

## Before you begin

Role required: sn\_icw.application\_admin or sn\_icw.admin

## Procedure

1.  Navigate to **All** &gt; **System Scheduler Schedules** and find the parent schedule that you need.

2.  Navigate to the **Schedule Entries** tab and select **New**.

3.  On the Schedule Entry form, fill in the fields.

    -   For the detailed description of schedule entry fields, see [Schedule entry fields](https://www.servicenow.com/docs/access?context=r_ScheduleEntryFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   Set the end time to one second less than a full hour to avoid overlap.
    -   The expected value for **Repeats** is **Daily**.
4.  Select **Submit**.


## Result

The production day has been created successfully and is displayed in the **sn\_icw\_industrial\_calendar.list** list.

The production day calendar record automatically includes a reference to the source schedule in the **source\_schedule** field. This reference is set when the calendar is generated and is system-managed. Non-admin users cannot modify this field.

**Parent Topic:**[Setting up prerequisites for Digital Factory Workspace](../concept/setting-up-prerequisites-digital-factory-workspace.md)

