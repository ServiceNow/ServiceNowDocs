---
title: Configure resources to load
description: Administrators can configure the number of resources to load on the calendar in Dispatcher Workspace so the page loads faster with fewer resources. Or the dispatcher can see more information at a glance if more resources are loaded.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure resources to load

Administrators can configure the number of resources to load on the calendar in Dispatcher Workspace so the page loads faster with fewer resources. Or the dispatcher can see more information at a glance if more resources are loaded.

## Before you begin

Role required: wm\_admin

## About this task

Before the Australia release, the system property `sn_fsm_disp_wrkspc.calendarCollapsedBehavior` controlled the behavior of whether all the groups, other than the first group, would be collapsed when Dispatcher Workspace loads. From the Australia release onwards the `sn_fsm_disp_wrkspc.calendarCollapsedBehavior` is removed and the behavior is controlled by the `sn_fsm_disp_wrkspc.dispatcher_workspace.calendar_resources_page_size`, which determines the number of resources that’s loaded on the page.

By default the calendar in Dispatcher Workspace shows 15 resources loaded on the calendar. You can update a system property to change the number of expanded resource schedules. The default value can be changed to a number between 1 and 100. However, if you enter a value over 30, there will be an impact on the page load time in Dispatcher Workspace.

The image below shows what Dispatcher Workspace looks like with the default number of resources added.

![Dispatcher workspace with the default resources loaded](../image/non-collapsed.png)

## Procedure

1.  Navigate to **All** and type `sys_properties.list`, then press Enter or Return on your keyboard.

2.  Search for and select the `sn_fsm_disp_wrkspc.dispatcher_workspace.calendar_resources_page_size` property.

3.  Change the property in the Value field to a number between 1-100.

    **Note:** Entering a number over 30 will impact Dispatcher Workspace load time.

4.  Select **Update**.


