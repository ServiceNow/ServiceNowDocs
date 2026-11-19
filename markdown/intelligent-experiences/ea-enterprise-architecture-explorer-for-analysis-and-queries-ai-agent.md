---
title: Enterprise Architecture explorer for analysis and queries AI agent
description: The agent answers questions about Enterprise Architecture data based on Common Service Data Model \(CSDM\) 5.0 entities and their relationships. It covers business capabilities, business applications, services, infrastructure, integrations, value streams, AI systems, technology standards, and conformance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ea-enterprise-architecture-explorer-for-analysis-and-queries-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture AI agents, Enterprise Architecture, AI agents library, AI assets, Enable AI experiences]
---

# Enterprise Architecture explorer for analysis and queries AI agent

The agent answers questions about Enterprise Architecture data based on Common Service Data Model \(CSDM\) 5.0 entities and their relationships. It covers business capabilities, business applications, services, infrastructure, integrations, value streams, AI systems, technology standards, and conformance.

## Workflow

The agent helps the user explore, analyze, and get answers about their Enterprise Architecture data.

1.  Interpret the user's question and identify the architecture entities it refers to. Ask for clarification only when required information is missing, such as which owner field the user means.
2.  Retrieve the requested data, such as application rationalization scores, capability health, technology risk, architectural artifacts, relationships between entities, and field-level details.
3.  Trace upstream or downstream dependencies from a named item when the user asks about impact or dependencies.
4.  For questions about missing relationships, such as applications with no assigned service, combine results from multiple queries to answer the question completely.
5.  Try alternative approaches when a query returns no results before reporting that no data was found.
6.  Present the answer in plain text with links to the relevant records, summarizing large result sets and offering to show more.
7.  Highlight notable patterns in the data, such as low scores or coverage gaps, and suggest two or three follow-up questions based on the results.

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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Enterprise Architecture Explorer Query Agent

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ea-ai-agents-overview.md)

**Related topics**  


[Exploring Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-overview.md)

[Working with Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-use.md)

[Enable Knowledge Graph system properties for the Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/set-kg-system-properties-ea-qna.md)

[Exploring ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

