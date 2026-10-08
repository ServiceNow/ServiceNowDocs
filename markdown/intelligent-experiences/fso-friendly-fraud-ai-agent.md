---
title: Friendly fraud AI agent
description: The agent guides the human agent through resolving a friendly fraud dispute. It recommends an action based on published guidance and similar past overrides, then supports the agent's decision with real-time context to keep resolutions accurate and compliant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-friendly-fraud-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Friendly fraud AI agent

The agent guides the human agent through resolving a friendly fraud dispute. It recommends an action based on published guidance and similar past overrides, then supports the agent's decision with real-time context to keep resolutions accurate and compliant.

## Workflow

The agent helps the human agent decide how to resolve a friendly fraud dispute.

1.  Look up the friendly fraud task and display its case, transaction, customer, and dispute amount details.
2.  Retrieve the knowledge article on resolving friendly fraud disputes and use it to determine a recommended action and reason.
3.  Record the recommended action and reason on the task.
4.  Check historical friendly fraud cases where the recommendation was overridden and surface up to two similar past examples.
5.  Present the recommendation, its reasoning, and any historical insight, then ask the agent to choose a resolution action — decline the dispute, issue a credit and write-off, or proceed with the dispute.
6.  If the agent's choice differs significantly from the recommendation, ask them to explain why.
7.  Draft rejection communication when the agent declines the dispute, and let the agent know what to do next.
8.  Update the task with the resolution taken and confirm with a closing message.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Check if friendly fraud task valid for further processing

Get recently closed friendly fraud tasks with overrides

Update friendly fraud recommended action and recommended action reason

Update friendly fraud resolution action taken

-   **Subflows**

Get friendly fraud task details

-   **Search retrievals**

Get knowledge article


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Friendly fraud resolving

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/fso-ai-agents-overview.md)

