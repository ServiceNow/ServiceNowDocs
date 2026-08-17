---
title: Company news &amp; events AI agent
description: This AI agent keeps users informed by sharing the latest updates on news, events, and announcements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/empx-company-news-events-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Employee Experience AI agents, Employee Experience, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Company news &amp; events AI agent

This AI agent keeps users informed by sharing the latest updates on news, events, and announcements.

## Workflow

The agent helps users complete tasks related to company news &amp; events.

1.  Retrieve latest news and events using extracted filters.
2.  If processedNews is empty or an empty response is returned from previous step, inform the user that no information has been found, and end the conversation.
3.  Display processedNews to the user.
4.  If NextPageToken is not null, ask the user whether they want to see more results, or if they would like more details about a specific news or event.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Generate news detailed response

Get latest news and events

Get next news and events

Take event action


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

nobody

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Employee Experience at [Unified Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/ec-and-ecpro-landing-page.md).

**Parent Topic:**[Employee Experience AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/employee-experience-ai-agents-overview.md)

