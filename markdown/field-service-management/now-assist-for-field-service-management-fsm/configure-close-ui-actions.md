---
title: Configure the Generate closure notes UI action
description: Add generative AI-specific functionality to the task closure screens by configuring the Generate closure notes UI action that is included with the Now Assist for Field Service Management \(FSM\) application.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for FSM]
---

# Configure the Generate closure notes UI action

Add generative AI-specific functionality to the task closure screens by configuring the Generate closure notes UI action that is included with the Now Assist for Field Service Management \(FSM\) application.

## Before you begin

Role required: admin

## About this task

The Field Service Management application includes Close complete and Close incomplete parameter screens that agents can use to close work order tasks.

The Now Assist for FSM application includes generative AI-specific functionality that agents can use to generate work order task closure summaries.

## Procedure

1.  Activate the Generate closure notes UI action for the Close complete screen.

    1.  Navigate to **All** &gt; **System Mobile** &gt; **Screens**.

    2.  Filter the list to display **Close** in the **Name** field.

    3.  Select the Close complete screen.

    4.  Select the **Actions** tab.

    5.  Select the **gen\_ai\_user\_action\_close\_complete** action.

    6.  Select the **Active** check box.

    7.  Select **Update**.

2.  Activate the Generate closure notes UI action for the Close incomplete screen.

    1.  Navigate to **All** &gt; **System Mobile** &gt; **Screens**.

    2.  Filter the list to display **Close** in the **Name** field.

    3.  Select the Close incomplete screen.

    4.  Select the **Actions** tab.

    5.  Select the **gen\_ai\_user\_action\_close\_incomplete** action.

    6.  Select the **Active** check box.

    7.  Select **Update**.


## Result

The Generate closure notes UI action is enabled. Agents can generate closure notes when closing work order tasks on the Mobile Agent® application. For more information, see [Generate work order task closure summaries in ServiceNow Agent](generate-close-now-assist-fsm.md).

