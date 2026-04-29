---
title: Schedule a callback for a customer
description: Schedule callbacks on behalf of customers from CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Callback requests by agents, Use omnichannel callback, Customer communication, Use, Customer Service Management]
---

# Schedule a callback for a customer

Schedule callbacks on behalf of customers from CSM Configurable Workspace.

## Before you begin

Ensure the following:

-   Customer Service Management \(CSM\) \[com.sn\_customerservice\] plugin is activated
-   Omnichannel Callback for Customer Service Management \(com.sn\_omnichannel\_callback\) plugin is installed
-   Appointment booking \[com.snc.appointment\_booking\] plugin is installed \(automatically installed with omnichannel callback \[sn\_callback\] plugin\)
-   System property **sn\_callback.enable\_agent\_scheduled\_callback** is enabled

Role required: sn\_omni\_callback.callback\_writer

## About this task

Agent-scheduled callbacks enable agents to create callback tasks while interacting with customers through any channel such as chat, voice, email, messaging, or case.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(![List icon to view callback list](../image/list-icon-callback.png)\)

3.  Open a case or interaction.

    **Note:** The case must be in the Open state or the interaction must be in WIP state.

4.  Select **Schedule Callback**.

5.  In the Schedule Callback widget, enter the required information.

6.  Select **Schedule**


## Result

-   A confirmation message displays indicating successful callback task creation.
-   A callback task is created with the state as Open.
-   The callback context shows the related case number \(if scheduled from a case\).

**Related topics**  


[View scheduled callbacks](view-scheduled-callbacks.md)

[View related callbacks in the contextual side panel](view-related-callbacks-contextual-side-panel.md)

[Reschedule a callback](reschedule-callback.md)

[Cancel a callback](cancel-callback.md)

