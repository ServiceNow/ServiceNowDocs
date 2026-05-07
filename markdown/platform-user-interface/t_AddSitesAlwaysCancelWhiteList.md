---
title: Add sites to the always cancel list
description: You can add UI pages or other links to the always cancel list so that users can cancel actions on these pages by navigating to another module or link.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Navigation action cancellation, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add sites to the always cancel list

You can add UI pages or other links to the always cancel list so that users can cancel actions on these pages by navigating to another module or link.

## Before you begin

Role required: admin

## About this task

User actions can always cancel items on the list. You should only add items to the list that provide read-only data to the user, such as a dashboard or a report.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter and press the Enter key.

2.  In the **Go to** field, select **Name**, enter `glide.request_manager.always_cancel`, and select **Go**.

3.  Select the property name to open it.

4.  In the **Value** field, add a comma-separated list of URIs you want to allow users to cancel.

5.  Select **Update**.


**Parent Topic:**[Navigation action cancellation](../concept/c_CancelingNavigationActions.md)

**Related topics**  


[Prevent users from canceling module transactions](t_PrevUsersCancelModTrans.md)

