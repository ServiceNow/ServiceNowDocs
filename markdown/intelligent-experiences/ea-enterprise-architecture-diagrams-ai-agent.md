---
title: Enterprise Architecture diagrams AI agent
description: The agent finds a business application by name or ID and generates a hierarchy diagram saved as a named architectural artifact. The agent also summarizes the generated diagram.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ea-enterprise-architecture-diagrams-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture AI agents, Enterprise Architecture, AI agents library, AI assets, Enable AI experiences]
---

# Enterprise Architecture diagrams AI agent

The agent finds a business application by name or ID and generates a hierarchy diagram saved as a named architectural artifact. The agent also summarizes the generated diagram.

## Workflow

The agent helps the user generate and review a hierarchy diagram for a business application.

1.  Look up the business application that the user names or identifies by ID.
2.  If no match is found, ask the user for the correct business application name or ID.
3.  If several matches are found, list them and ask the user to select one.
4.  Ask the user for an artifact name for the diagram, and ask for a different name if an artifact with that name already exists.
5.  Generate the hierarchy diagram for the selected business application.
6.  Present a link to the generated diagram so the user can review it.
7.  Generate and display a summary of the diagram.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Generate Business Application Summary

Generate Diagram URL

Lookup Business Application


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_apm.apm\_user

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Generate enterprise architecture diagram

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ea-ai-agents-overview.md)

**Related topics**  


[Enterprise Architecture AI agent diagramming agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-aiagents-ea-diagramming-usecase.md)

[Exploring ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

