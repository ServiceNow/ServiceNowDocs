---
title: User impact analysis AI Agent
description: This agent investigates incidents and cases related to the alerts and affected services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aiops-user-impact-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [AIOps and AIOps Leap AI agents, AIOps and AIOps Leap, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# User impact analysis AI Agent

This agent investigates incidents and cases related to the alerts and affected services.

## Workflow

The agent helps users complete tasks related to user impact analysis.

1.  Check if &lt;offering\_ids&gt; and &lt;service\_ids&gt; are NOT defined, then return from the agent silently.
2.  If &lt;offering\_ids&gt; and &lt;service\_ids&gt; are BOTH empty, then return from the agent silently.
3.  Run the 'Fetch related issues' tool.
4.  Check if &lt;incidents&gt; and &lt;cases&gt;, returned in step 3, are empty.
5.  Run the "Format related issues summary" tool.
6.  Write the formatted summary to the alert worknote.
7.  Pass the &lt;offering\_ids&gt; and &lt;service\_ids&gt; values to the next agent.

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

-   **Capability**

Alert impact analysis

-   **Script**

Display empty incidents and cases message

Fetch related issues

Format related issues summary

Write worknote to alert


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles

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

Analyze alert impact - New

</td></tr></tbody>
</table>Learn more about Learning Enhanced Automation Platform \(LEAP\) at [Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap.md).

**Parent Topic:**[AIOps and AIOps Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aiops-ai-agents-overview.md)

