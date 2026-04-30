---
title: Disable the Connect overlay
description: The Connect overlay is enabled by default and is integrated with the standard user interface. You can disable the Connect overlay.
locale: en-US
release: xanadu
product: Connect
classification: connect
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable the Connect overlay

The Connect overlay is enabled by default and is integrated with the standard user interface. You can disable the Connect overlay.

## Before you begin

Role required: admin

## About this task

To disable the Connect overlay and remove the toggle Connect sidebar icon from the banner frame, set the **collaboration.frameset** property to **false**.

## Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Administration** &gt; **Properties**.

2.  Locate the property called **Enable Connect in the frameset** \(**collaboration.frameset**\) and clear the check box.

3.  Click **Save**.


## Result

When the frameset is disabled, any Connect chats open in the Connect workspace. For more information on completely disabling Connect Chat, see [Disable Connect Chat](../concept/c_CollaborationAdministration.md#).

