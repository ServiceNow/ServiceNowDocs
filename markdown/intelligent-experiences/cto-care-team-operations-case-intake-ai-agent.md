---
title: Care Team Operations case intake AI agent
description: This workflow guides users through submitting operational issues by prompting for a clear problem description and ensuring required details—such as location, requesting unit, asset tag, and priority—are captured. It intelligently detects and separates multiple requests in a single user utterance, summarizes each request with its details, and confirms accuracy with the user before proceeding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cto-care-team-operations-case-intake-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Care Team Operations AI agents, Care Team Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Care Team Operations case intake AI agent

This workflow guides users through submitting operational issues by prompting for a clear problem description and ensuring required details—such as location, requesting unit, asset tag, and priority—are captured. It intelligently detects and separates multiple requests in a single user utterance, summarizes each request with its details, and confirms accuracy with the user before proceeding.

## Workflow

The agent helps users complete tasks related to care team operations case intake.

1.  Fetch requesting units.
2.  Prompt for issue details.
3.  Identify distinct requests.
4.  Classify case types.
5.  Get remaining information.
6.  Generate request summaries.
7.  Validate request summaries.
8.  Create Care Team Operations case.

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

-   **Search retrieval**

Get relevant knowledge articles

-   **Script**

Requesting Unit Lookup


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_hco.care\_team\_manager, sn\_hco.care\_team\_member

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

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Request care team assistance

</td></tr></tbody>
</table>Learn more about Healthcare Operations at [Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-overview.md).

**Parent Topic:**[Care Team Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/care-team-operations-ai-agents-overview.md)

