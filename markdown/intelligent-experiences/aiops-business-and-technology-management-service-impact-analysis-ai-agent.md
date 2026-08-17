---
title: Business and technology management service impact analysis AI agent
description: This agent calculates the business and technology management services impacted by a given alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aiops-business-and-technology-management-service-impact-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [AIOps and AIOps Leap AI agents, AIOps and AIOps Leap, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Business and technology management service impact analysis AI agent

This agent calculates the business and technology management services impacted by a given alert.

## Workflow

The agent helps users complete tasks related to business and technology management service impact analysis.

1.  Check if &lt;impacted\_service\_instances&gt; is defined; if not defined, then return from the agent.
2.  Check if &lt;impacted\_service\_instances&gt; is empty, then return from the agent.
3.  Run the 'Related offerings and services' tool.
4.  Check if &lt;offering\_message&gt; is defined.
5.  Check if &lt;service\_message&gt; is defined.
6.  Write the &lt;offering\_message&gt; and &lt;service\_message&gt; to the alert worknotes.
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

-   **Scripts**

Display Business/Technology services message

Display empty offering or services message

Display offering message

Related offerings and services

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

