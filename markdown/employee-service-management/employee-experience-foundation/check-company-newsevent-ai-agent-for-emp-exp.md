---
title: Company News &amp; Events AI Agent
description: Use this agent to enable users to check their company-related latest news and upcoming events.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use AI Agents, Now Assist for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Company News &amp; Events AI Agent

Use this agent to enable users to check their company-related latest news and upcoming events.

Verify that you have the following plugins:

-   Now Assist for Employee Experience version 2.0.3 and later.

    The AI Agents for Employee Experience is automatically installed with the updated version.

-   Content Publishing version 36.0.4 \(Installed automatically as part of Employee Center Pro\)

**Important:** To display the AI agent output to users in the Virtual Agent conversations, you must set the system property **sn\_aia.enable\_va\_conversation** value to **true**. By default, the property is set to **false**.

![Checking company events in Now Assist](../images/uex-aiagent-event.png)![Checking more details about a specify event in Now Assist.](../images/uex-aiagent-eventtopic.png)![Latest news and events in Now Assist.](../images/uex-aiagent-steps.png)

## Company News &amp; Events AI Agent overview

The **Company News &amp; Events AI Agent** helps users stay informed by sharing the latest updates on news, events, and announcements.

It understands general questions like "What’s the latest news?" or "Are there any upcoming events?", casual questions like "show me New York news" or "what's happening in Atlanta this month," and also specific questions such as "Get the latest news on 401k," "Show me events happening in New York," or "Show local news."

On prompting, it also provides updates based on the user’s location and their interests. Shows nearby events, local news stories, company updates, and news related to relevant people or topics the user cares about.

The agent helps users stay informed at all levels, from local to global.

## View Company News &amp; Events AI Agent in AI Agent Studio

To view the AI Agent, do the following:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Company News &amp; Events AI Agent**.

To activate, refer to [Activate Company News and Events AI Agent](../task/enable-company-news-and-events-ai-agent.md).

## Tools used by Company News &amp; Events AI Agent

|Name|Type|Execution mode|Display output|
|----|----|--------------|--------------|
|Take event action|Scripts|Autonomous|true|
|Get next news and events|Scripts|Autonomous|false|
|Generate news detailed response|Scripts|Autonomous|true|
|Detail summary generator|Scripts|Autonomous|false|
|Get latest events|Scripts|Autonomous|false|
|Summarise news and events|Scripts|Autonomous|false|
|Content processor|Scripts|Autonomous|true|
|Get Filters|Scripts|Autonomous|false|
|Get latest news|Scripts|Autonomous|false|

