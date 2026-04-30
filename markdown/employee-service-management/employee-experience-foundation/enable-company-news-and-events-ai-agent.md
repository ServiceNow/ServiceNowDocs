---
title: Activate Company News and Events AI Agent
description: Activate the Company News and Events AI Agent to enable users to check news and events in Now Assist in Virtual Agent.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-09-01"
reading_time_minutes: 1
breadcrumb: [Company News &amp; Events AI Agent, Use AI Agents, Now Assist for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Activate Company News and Events AI Agent

Activate the Company News and Events AI Agent to enable users to check news and events in Now Assist in Virtual Agent.

## Before you begin

Role required: admin

## About this task

Enable the system property to display the AI agent output to users in the Now Assist in Virtual Agent conversations. In the AI Agent Studio, configure where the AI agent must display.

## Procedure

1.  Configure where the AI agent must display.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

    2.  Select **Company News &amp; Events AI Agent**.

    3.  In **Toggle display**, do the following:

        -   Verify that the **Status** of the AI agent is active.
        -   In the **Select display** section, do the following:
            1.  In **Assistants where AI agents are discoverable**, select **Now Assist in Virtual Agent \(default\)**.
            2.  Enable the **Display** option.
2.  Modify the **sn\_aia.enable\_va\_conversation** system property.

    1.  Search for `sys_properties.list` in the navigation.

        A list of all the system properties are displayed.

    2.  Search and select **sn\_aia.enable\_va\_conversation**.

    3.  Set the **Value** to **true**.


## Result

The **Company News &amp; Events AI Agent** is activated for users to check their news and events in the Now Assist in Virtual Agent.

