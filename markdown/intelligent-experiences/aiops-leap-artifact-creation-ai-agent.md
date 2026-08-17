---
title: Artifact creation agent AI agent
description: Assists in creating and viewing artifacts such as problem records, knowledge base articles, and playbooks for an automation opportunity. The agent checks for an automation opportunity number and invokes the artifact creation topic tool to generate the required artifacts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aiops-leap-artifact-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [AIOps and AIOps Leap AI agents, AIOps and AIOps Leap, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Artifact creation agent AI agent

Assists in creating and viewing artifacts such as problem records, knowledge base articles, and playbooks for an automation opportunity. The agent checks for an automation opportunity number and invokes the artifact creation topic tool to generate the required artifacts.

## Workflow

The agent creates automation opportunity artifacts by invoking the artifact creation topic tool with the appropriate context.

1.  Check whether an automation opportunity number is available and, if found, assign it to the artifact creation tool as input context.
2.  Invoke the artifact creation topic tool to generate the required artifacts, using optional parameters for the detail page URL and continuation options.
3.  Exit the workflow after artifact creation is complete.

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

-   **Conversational topic \(Virtual Agent\)**

artifact creation topic


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_itom\_leap.leap\_genai\_worker

</td></tr><tr><td>

Data access roles

</td><td>

sn\_itom\_leap.artifact\_creator\_agent

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

LEAP agent

</td></tr></tbody>
</table>Learn more about Learning Enhanced Automation Platform \(LEAP\) at [Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap.md).

**Parent Topic:**[AIOps and AIOps Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aiops-ai-agents-overview.md)

