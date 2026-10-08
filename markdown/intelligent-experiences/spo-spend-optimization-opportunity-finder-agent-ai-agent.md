---
title: Spend Optimization Opportunity Finder agent
description: This Sourcing and Procurement Operations agent compares on-contract and off-contract purchase order pricing to identify savings opportunities, quantifying the potential savings from redirecting off-contract spend to existing supplier contracts. It can also answer follow-up questions about spend data, contracts, savings opportunities, pipeline projects, and savings calculations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spo-spend-optimization-opportunity-finder-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Sourcing and Procurement Operations AI agents, Sourcing and Procurement Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Spend Optimization Opportunity Finder agent

This Sourcing and Procurement Operations agent compares on-contract and off-contract purchase order pricing to identify savings opportunities, quantifying the potential savings from redirecting off-contract spend to existing supplier contracts. It can also answer follow-up questions about spend data, contracts, savings opportunities, pipeline projects, and savings calculations.

## Workflow

1.  When run as a scheduled job, use the OffContractSpendAnalyzer tool to compare on-contract and off-contract purchase order pricing and create savings opportunities.
2.  When a user creates a pipeline project from a savings opportunity, show pre-filled details, collect changes and priority, then run the Create Pipeline Project tool after confirmation.
3.  Offer to generate a chat summary of the session and, if the user agrees, post it to the pipeline project's work notes.
4.  For any other question about spend data, contracts, savings opportunities, pipeline projects, or savings calculations, run the SpendIntelligenceTool to answer.

<table id="table_gjz_p3c_tkc"><thead><tr><th>

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

-   **Script**

OffContractSpendAnalyzer

Create Pipeline Project

SpendIntelligenceTool


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_spend\_gen\_ai.now\_assist\_fulfiller, sn\_shop.procurement\_specialist, sn\_spend\_mgmt.category\_manager\_admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_spend\_gen\_ai.now\_assist\_fulfiller, sn\_shop.procurement\_specialist, sn\_spend\_mgmt.category\_manager\_admin

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

Savings Opportunity Discovery

</td></tr></tbody>
</table>Learn more about Sourcing and Procurement Operations at [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/psm-overview.md).

**Parent Topic:**[Sourcing and Procurement Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/spo-ai-agents-overview.md)

