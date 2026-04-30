---
title: Wrap up configuration
description: Set up the wrap up configuration.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Wrap up overview, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Wrap up configuration

Set up the wrap up configuration.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Interaction** &gt; **Wrap Up Configuration**.

    The Interaction Wrap Up Configurations screen appears.

2.  If this is the first time you are setting up the wrap up configuration

    1.  Select **Wrap Up for Chat Interactions**.
    2.  On the Wrap Up for Chat Interactions screen, select **Active**.
    3.  Select **Update** or configure other options on the screen.
3.  Do one of the following:

    -   To edit an existing record, select the name of the record.
    -   To create a new record, select **New**.
4.  Fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the wrap up configuration.|
    |Application| |
    |Table| |
    |Active|Indicates whether wrap up is enabled.|
    |Order|Value of this configuration relative to the other configurations.|
    |Conditions|Set the conditions that define the class of interactions that use this configuration.|

5.  In the Duration tab, configure the wrap up duration settings:

    -   Enforce wrap up duration - if selected, the agent will have a limited length of time \(defined in the **Duration in seconds** field\) to enter wrap up information.
    -   Show duration to agent - this field appears only if you selected **Enforce wrap up duration** and indicates whether the wrap up duration displays on the screen for the agent.
    -   Duration in seconds - this field appears only if you selected **Enforce wrap up duration** and defines the length of time \(in seconds\) that the agent has to wrap up the interaction.
6.  In the Codes tab, configure the wrap up codes:

    -   Enable wrap-up codes - if selected, the agent can enter pre-defined wrap up codes when they close an interaction.
    -   Default wrap-up code - this field appears only if you selected **Enforce wrap up codes** and indicates the default wrap up code.
    -   Allowed wrap-up codes - this field appears only if you selected **Enforce wrap up codes** and lists all of the wrap up codes that an agent can use.
7.  Select **Update** if you are updating an existing configuration or **Submit** if you are creating a new configuration.


**Parent Topic:**[Wrap up overview](../concept/wrap-up-overview.md)

