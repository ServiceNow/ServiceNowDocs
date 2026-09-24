---
title: Enterprise Architecture explorer for analysis and queries AI agent
description: This AI agent explores and analyzes Enterprise Architecture data across all 7 CSDM 5.0 domains. It answers questions about business capabilities, applications, services, infrastructure, integrations, value streams, AI systems, technology standards, and compliance using Knowledge Graph.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ea-enterprise-architecture-explorer-for-analysis-and-queries-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture AI agents, Enterprise Architecture, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Enterprise Architecture explorer for analysis and queries AI agent

This AI agent explores and analyzes Enterprise Architecture data across all 7 CSDM 5.0 domains. It answers questions about business capabilities, applications, services, infrastructure, integrations, value streams, AI systems, technology standards, and compliance using Knowledge Graph.

## Workflow

The agent answers questions about enterprise architecture data captured in the ServiceNow CSDM 5.0 model.

1.  Determine whether the question is about a single entity, a list, a count, or a relationship between entities, such as which applications support a capability.
2.  Ask the user to clarify which specific field they mean if a question refers to an ambiguous field, such as "owner."
3.  Query the appropriate underlying data source for the type of question, such as portfolio scores and ratings, relationships between entities, capability health, technology risk, or architecture artifacts.
4.  For questions about missing relationships, such as applications with no assigned service, combine results from multiple queries to answer the question completely.
5.  Present the answer directly, with entity names linked to their records, and suggest a few relevant follow-up questions based on the results.
6.  Continue the conversation for follow-up questions, and only finish when the user explicitly confirms they are done.

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

-   **Scripts**

App Rationalization Query

Artifact Entity Resolver

Capability Hierarchy App Resolver

Related Entities Resolver

-   **Knowledge Graph**

EA Knowledge Graph


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_apm.apm\_read, sn\_apm.apm\_user

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_apm.apm\_read, sn\_apm.apm\_user

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

-   Enterprise Architecture Explorer Query Agent
-   Default VA Workflow

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ea-ai-agents-overview.md)

