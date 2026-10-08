---
title: Create a sub-agent
description: Create a custom sub-agent to hand off a specialized task, such as code review or security analysis, to a reusable agent with focused instructions and limited access. A narrow scope helps produce consistent results, limiting the sub-agent to only the skills and MCP servers it requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-sub-agent.html
release: zurich
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [sub-agents, custom sub-agent, system prompt]
breadcrumb: [Extend ServiceNow Cowork, Use, ServiceNow Cowork, Enable AI experiences]
---

# Create a sub-agent

Create a custom sub-agent to hand off a specialized task, such as code review or security analysis, to a reusable agent with focused instructions and limited access. A narrow scope helps produce consistent results, limiting the sub-agent to only the skills and MCP servers it requires.

## Before you begin

Role required: sn\_app\_cowork.user

## Procedure

1.  Navigate to **Settings** &gt; **Sub-Agents**.

2.  Select the add icon.

    The **New Sub-Agent** dialog opens.

3.  Enter the sub-agent details.

    |Field|Description|
    |-----|-----------|
    |**Name \(slug format\)**|Unique name in lowercase letters and hyphens only, used to reference the sub-agent in `spawn_subagent`.|
    |**Description**|A short summary of what the sub-agent does.|
    |**Skills \(optional\)**|The skills the sub-agent can use.|
    |**MCP Servers \(optional\)**|The MCP servers the sub-agent can use.|
    |**System Prompt \(Markdown\)**|Instructions that define the sub-agent's role and guidelines.|

4.  Select **Create**.

5.  Select the refresh icon to reload the list after you add or change a sub-agent.

6.  Select the folder icon to open the folder where sub-agents are stored.


## Result

The new sub-agent appears in the **Sub-Agents** list.

**Parent Topic:**[Extend ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/extending-cowork.md)

