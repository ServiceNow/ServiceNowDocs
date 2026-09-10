---
title: SRE investigate AI agent
description: This AI agent coordinates investigation activities across multiple observability platforms by orchestrating tool-specific agents, such as Dynatrace, New Relic, Kentik, SolarWinds, Splunk, AWS, ThousandEyes, and LogicMonitor. It correlates findings, identifies root causes, and synthesizes comprehensive investigation reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-sre-investigate-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# SRE investigate AI agent

This AI agent coordinates investigation activities across multiple observability platforms by orchestrating tool-specific agents, such as Dynatrace, New Relic, Kentik, SolarWinds, Splunk, AWS, ThousandEyes, and LogicMonitor. It correlates findings, identifies root causes, and synthesizes comprehensive investigation reports.

## Workflow

The agent coordinates a full investigation of an alert across multiple observability platforms and produces a consolidated report.

1.  Determine whether the request is a new investigation or a follow-up question on a previous investigation already in the conversation.
2.  For a new investigation, identify the vendor-specific tool agents relevant to the alert and invoke them, collecting data in parallel where possible.
3.  Correlate the findings returned by each tool agent, gracefully handling any tool agent that fails to return results.
4.  Identify the probable root cause and compile supporting evidence into a structured investigation report with recommended actions and suggested follow-up questions.
5.  Save the investigation analysis and insight to the alert record so the findings persist beyond the conversation.
6.  For follow-up questions, answer using the existing investigation findings without repeating the full investigation or the save steps.

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

Retrieve a report of observability metadata from the em\_alert record

-   **Scripts**

Find Vendors Referencing Entity

Read SO Service Analysis

Save GAI Insight

Save SRE Analysis


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

evt\_mgmt\_operator, connection\_admin

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

[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom-agentic-aia.md)

</td></tr></tbody>
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

