---
title: Procurement inquiry analysis AI agent
description: This Sourcing and Procurement Operations agent is an educational assistant for procurement and sourcing terminology questions. The agent scans policy manuals and help articles to deliver plain-language explanations of purchase orders, requisitions, sourcing requests, and procurement cases. It can connect users to a live agent if knowledge articles don't have sufficient information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spo-procurement-inquiry-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Sourcing and Procurement Operations AI agents, Sourcing and Procurement Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Procurement inquiry analysis AI agent

This Sourcing and Procurement Operations agent is an educational assistant for procurement and sourcing terminology questions. The agent scans policy manuals and help articles to deliver plain-language explanations of purchase orders, requisitions, sourcing requests, and procurement cases. It can connect users to a live agent if knowledge articles don't have sufficient information.

## Workflow

1.  When the user asks about policies, requisitions, sourcing processes, or supplier eligibility, search for relevant knowledge articles and present the information with a link to the source article.
2.  If no knowledge article answers the question, try connecting to a live agent. If no live agent is available, redirect to the Employee Center as a last resort.
3.  Ask if the user has additional questions and continue or exit accordingly.

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

-   **Conversational topic**

Connect to Live Agent

-   **Script**

Redirect to Employee Center

-   **Search Revtieval**

Get relevant knowledge articles


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_spend\_gen\_ai.now\_assist\_requester

</td></tr><tr><td>

Data access roles

</td><td>

sn\_spend\_gen\_ai.now\_assist\_requester, sn\_shop.shopper, sn\_spend\_psd.requestor

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

Help fulfill procurement requests

</td></tr></tbody>
</table>Learn more about Sourcing and Procurement Operations at [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/psm-overview.md).

**Parent Topic:**[Sourcing and Procurement Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spo-ai-agents-overview.md)

