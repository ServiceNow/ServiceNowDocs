---
title: Error analysis and remediation AI agent
description: This AI agent is helps admins and operators investigate Error Framework error codes, analyze root causes, and execute preconfigured remediation actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-err-error-analysis-and-remediation-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Error analysis and remediation AI agent

This AI agent is helps admins and operators investigate Error Framework error codes, analyze root causes, and execute preconfigured remediation actions.

## Workflow

The agent helps admins and operators investigate and remediate errors within the ServiceNow Error Framework.

1.  Determine whether the user's request is about investigating an error or remediating one. If the user is viewing an Error Framework page, automatically identify the relevant error code for context.
2.  For investigation requests, retrieve and summarize matching errors in a compact table, or provide a deeper analysis of a specific error code, including root cause and business impact, when the user asks for it.
3.  For remediation requests, gather full context on the error and select the specific action that best matches the root cause, or provide manual steps and state-management options if no automated action is available.
4.  Present the proposed action to the user, including the error code, action, reason, and scope, and confirm before proceeding.
5.  Execute the approved action, report the results and a tracking link, and suggest any related follow-up actions.
6.  If a request falls outside the Error Framework, or asks for an unsupported destructive operation, let the user know and offer to help with a supported task instead.

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

-   **Generative AI skill**

ai\_insights\_skill

-   **Scripts**

execute\_remediation\_action

get\_errors\_by\_user\_query

get\_errors\_for\_error\_code

get\_error\_code\_data

resolve\_ef\_page\_context

-   **Knowledge Graph**

error\_framework\_schema


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

error\_framework.admin, error\_framework.operator

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

error\_framework.admin, error\_framework.operator

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

-   Error Analysis and Remediation Workflow
-   Pattern Diagnostic Workflow

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-ai-agents-overview.md)

