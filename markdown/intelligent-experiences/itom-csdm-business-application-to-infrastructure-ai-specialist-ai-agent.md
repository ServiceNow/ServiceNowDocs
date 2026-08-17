---
title: CSDM business application to infrastructure AI specialist
description: This AI specialist finds the best matching discovered service for each business application and creates the standard CSDM "Uses::Used by" relationship in the CI relationships table \[cmdb\_rel\_ci\].
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-csdm-business-application-to-infrastructure-ai-specialist-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Operations Management AI agents, IT Operations Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CSDM business application to infrastructure AI specialist

This AI specialist finds the best matching discovered service for each business application and creates the standard CSDM "Uses::Used by" relationship in the CI relationships table \[cmdb\_rel\_ci\].

## Workflow

The specialist connects the CSDM business application to infrastructure.

1.  Receive the user's request and search based on that filter.
2.  Evaluate and rank search results.
3.  Return the highest-ranking results or update the relevant record.

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

Agent Tool: Connect Business App to Application Service

Agent Tool: Get Business Applications

Agent Tool: Search Discovered Services by AI

Record Connection Runs


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

service\_mapping\_ai\_user, cmdb\_read, itom\_admin, snc\_internal, snc\_required\_script\_writer\_permission, sn\_bm\_client.benchmark\_data\_viewer, sn\_itom\_license.reader

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
</table>Learn more about IT Operations Management at [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

