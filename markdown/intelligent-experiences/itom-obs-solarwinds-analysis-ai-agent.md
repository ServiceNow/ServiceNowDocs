---
title: SolarWinds analysis AI agent
description: This AI agent fetches the details related to a SolarWinds alert by executing SWQL queries against SolarWinds to resolve the affected entity and retrieve supporting diagnostic information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-solarwinds-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# SolarWinds analysis AI agent

This AI agent fetches the details related to a SolarWinds alert by executing SWQL queries against SolarWinds to resolve the affected entity and retrieve supporting diagnostic information.

## Workflow

The agent investigates a SolarWinds alert by resolving the affected entity and querying SolarWinds for supporting details.

1.  Resolve the identifier provided, such as a node ID, application ID, IP address, hostname, or entity name, into a specific SolarWinds node or application.
2.  Confirm that a valid identifier was provided before proceeding, and stop with a clear message if one was not.
3.  Execute the appropriate SWQL queries against SolarWinds to retrieve details for the resolved entity, running independent queries in parallel where possible.
4.  Compile the retrieved data into findings and return them to the calling agent.

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

-   **Flow Action**

Execute SolarWinds SWQL Query

-   **File Upload**

SolarWinds Query Guide


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

evt\_mgmt\_operator

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
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

