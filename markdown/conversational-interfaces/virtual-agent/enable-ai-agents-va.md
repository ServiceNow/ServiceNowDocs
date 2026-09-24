---
title: Enable AI agents in Virtual Agent
description: Create and configure multiple assistants with specific scope and map the assistants to one or more portals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/enable-ai-agents-va.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure agentic conversations, Configure, Virtual Agent, Conversational Interfaces]
---

# Enable AI agents in Virtual Agent

Create and configure multiple assistants with specific scope and map the assistants to one or more portals.

## Before you begin

Role required: admin or virtual\_agent\_admin

**Note:** When a Virtual Agent conversation is triggered, any updates or comments in the record's work notes display as the AI agent rather than the user who initiated the conversation.

## Procedure

1.  Do one of the following:

2.  1.  Create an assistant in Assistant Designer or use a default assistant.

    For more information, see [Create a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-assistant.md).

2.  Assign the assistant to a specific portal or portals.

    For more information, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/display-assistant-portal-channel.md).

3.  Ensure that the **AI agents** skill is added to the assistant.

    In the assistant settings in Assistant Designer, select the **Agentic support** page, and select the **Prioritize AI agents during skills discovery** check box.

    \[Omitted image "assistant-skill.png"\] Alt text: In the assistant settings, ensure that the Prioritize AI agents during skills discovery option is enabled on the Agentic support tab.

4.  Map or publish an AI agent to one or more assistants in AI Agent Studio to make the agent available within a specific assistant.

    \[Omitted image "va-card-ai-agent.png"\] Alt text: Specify an assistant for the AI agent in the Select channels and status screen in AI Agent Studio.

    For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-next-best-action-agent.md).


## Result

During execution, only the configured AI agents are considered for the current assistant and dynamically makes them available to the Orchestrator for planning.

