---
title: Care Team Operations case creation AI voice agent
description: This agent helps healthcare staff report and submit Care Team Operations \(CTO\) requests. Trigger this agent when a user mentions Care Team Operations, CTO, or asks to submit a care team request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cto-care-team-operations-case-creation-voice-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Care Team Operations AI agents, Care Team Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Care Team Operations case creation AI voice agent

This agent helps healthcare staff report and submit Care Team Operations \(CTO\) requests. Trigger this agent when a user mentions Care Team Operations, CTO, or asks to submit a care team request.

## Workflow

The agent helps users complete tasks related to care team operations case creation voice.

1.  Get the requesting unit of the user.
2.  Ask the user to describe their issue.
3.  Use the Get Relevant Knowledge Articles tool with the query "Case Definition" to classify the issue.
4.  Collect any remaining required fields mentioned in the knowledge article one at a time based on &lt;case\_type&gt;.
5.  Use the Get Service Definitions tool with &lt;case\_type&gt; as a JSON array.
6.  Say, "Let me confirm the details of your request before I submit." Read out the details to the user.
7.  Say, "Let me create your request." Create the Care Team Operations case using &lt;requesting\_unit&gt;, &lt;case\_type&gt;, &lt;issue\_description&gt;, &lt;location&gt;, &lt;asset\_tag&gt;, &lt;priority&gt;, and all additional fields collected.
8.  End the conversation by saying, "Thank you for contacting Care Team Operations assistant."

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

Create care team operation cases

Get service definition details

Requesting Unit Lookup

-   **Search retrieval**

Get relevant knowledge articles


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_hco.care\_team\_member, sn\_hco.care\_team\_manager

</td></tr><tr><td>

Data access roles

</td><td>

sn\_hco.care\_team\_member, sn\_hco.care\_team\_manager

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Healthcare Operations at [Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-overview.md).

**Parent Topic:**[Care Team Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/care-team-operations-ai-agents-overview.md)

