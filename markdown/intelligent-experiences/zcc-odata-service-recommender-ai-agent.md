---
title: OData service recommender AI agent
description: This AI agent is used to recommend SAP OData services and create models from them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/zcc-odata-service-recommender-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Zero Copy Connector for ERP AI agents, Zero Copy Connector AI agents, AI agents library, AI assets, Enable AI experiences]
---

# OData service recommender AI agent

This AI agent is used to recommend SAP OData services and create models from them.

## Workflow

1.  Determine the type of request: read, create, or update only.
2.  Verify that the request maps to exactly one SAP OData V2 service.
3.  Check the internal SAP OData service catalog and attempt to match the user request against catalog entries using intent keywords and domain.
4.  Resolve the request, if possible.
5.  If the request is broad or ambiguous, suggest refinement.
6.  Validate the SAP OData V2 technical service name and begin discovery.
7.  Final response and execution.

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

Existing model checker

Model operation URL generator

Read endpoints

-   **Subflows**

OData Service Checker

Model Creator

-   **Web search**

Use web search


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_erp\_integration.erp\_ai\_user, sn\_erp\_integration.erp\_admin

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
</table>Learn more at [ServiceNow Otto for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md) and [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-overview.md).

**Parent Topic:**[Zero Copy Connector for ERP AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/zcc-ai-agents-overview.md)

