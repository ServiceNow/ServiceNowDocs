---
title: OData service recommender AI agent
description: This Workflow Data Fabric agent is used to recommend SAP Odata services and create models from them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-zcc-odata-service-recommender-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# OData service recommender AI agent

This Workflow Data Fabric agent is used to recommend SAP Odata services and create models from them.

## Workflow

1.  Determine whether the user's request is a Read, Create, or Update operation.
2.  Determine whether the request maps cleanly to exactly one SAP OData V2 service and one entity, versus spanning multiple domains or services \(which makes it "broad"\).
3.  Before searching the web, check if the request matches a known service in the internal catalog; use that match if exactly one is found.
4.  If no catalog match exists, search api.sap.com to identify exactly one technical service name. Retry the search \(up to twice\) with more specific business terms if the result is ambiguous.
5.  If the request spans multiple services/domains, ask the user to pick from a short list of narrowed options. Once the user selects an option, restart resolution from the web-search step using their selection.
6.  Confirm the identified service technical name. If only a deprecated service exists, ask the user to explicitly confirm before proceeding.
7.  Look up the specific entity endpoint for the validated service and CRUD type. If none or multiple match, fetch fresh service metadata and retry, or fall back to suggesting refinement.
8.  Present a plain-language \(never raw JSON\) summary confirming the service, deprecation status, CRUD type, and endpoint outcome.
9.  Check for an existing model matching the resolved service/endpoint. Let the user reuse it or create one, then provide a link to the result.

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

Model Creator

OData Service Checker

-   **Web search**

Use web search


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

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

None

</td></tr></tbody>
</table>Learn more about Workflow Data Fabric at [Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

**Parent Topic:**[Workflow Data Fabric AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/wdf-ai-agents-overview.md)

