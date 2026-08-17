---
title: Calculation operand AI agent
description: This AI agent identifies and returns relevant metric definitions and emission factors from existing sources. It replaces generic references with precise metric definitions and emission factor names in the input formula.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ops-calculation-operand-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Operational Sustainability Management AI agents, Operational Sustainability Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Calculation operand AI agent

This AI agent identifies and returns relevant metric definitions and emission factors from existing sources. It replaces generic references with precise metric definitions and emission factor names in the input formula.

## Workflow

The agent helps users complete tasks related to calculation operand.

1.  Use the formula stored in \{emissions\_formula\} and copy it into $\{emissions\_formula\_internal\}. Store both values in memory.
2.  Read the formula from left to right, consuming one sub-expression at a time.
3.  Identify each unresolved element, one at a time, within the current sub-expression.
4.  Search metric definitions and show results.
5.  Search emission factor and show results.
6.  Continue within the current sub-expression.
7.  Continue to the next sub-expression.
8.  When all sub-expressions are resolved, present the final \{emissions\_formula\} without additional commentary.

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

-   **Search retrievals**

Get emission factors

Get metric definition

-   **Script**

Replace selected choices in formula


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esg\_gen\_ai.cmd\_agent\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_esg.reader

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

Generate carbon calculations for metrics

</td></tr></tbody>
</table>Learn more about Operational Sustainability Management at [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md).

**Parent Topic:**[Operational Sustainability Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ops-ai-agents-overview.md)

