---
title: Using AI Agents with Now Assist for Employee Experience
description: Use AI Agents with the Now Assist for Virtual Agent in the Employee Center for users to have a seamless agent-like conversation.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Using AI Agents with Now Assist for Employee Experience

Use AI Agents with the Now Assist for Virtual Agent in the Employee Center for users to have a seamless agent-like conversation.

Verify that you have the following plugins:

-   Now Assist for Employee Experience version 2.0.3 and later. The AI Agents for Employee Experience is automatically installed with the updated version.
-   Content Publishing version 36.0.4 \(Installed automatically as part of Employee Center Pro\)

<table id="table_o2p_xw3_jgc"><thead><tr><th>

Agent name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company News &amp; Events AI Agent

</td><td>

This Agent shares the latest updates on news, events, and announcements. It can understand and respond to general questions like 'What’s the latest news?' or 'Are there any upcoming events?'

</td></tr></tbody>
</table>## System properties

To display the AI agent output to users in the Now Assist in Virtual Agent conversations, you must set the system property **sn\_aia.enable\_va\_conversation** value to **true**. By default, the property is set to **false**.

The properties are listed in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation context-menu filter.

<table id="table_y5g_tw5_jgc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.enable\_va\_conversation

</td><td>

Set this property to **true** to display the AI agent output to users while using the Now Assist in Virtual agent in the Employee Center.-   Type: true/false
-   Default value: False

</td></tr></tbody>
</table>**Important:** All use case and AI agent records are read only by default.

To run the AI agents autonomously, you must first duplicate the use case, and then do the following steps:

-   Activate the use case.
-   Activate all agents within the use case.
-   Activate the trigger to invoke the use case automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

