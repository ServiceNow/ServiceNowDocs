---
title: Contract repository AI agent
description: This AI agent retrieves contract repository details for a specified record, including vendor information, contract model, and document attachment IDs. It also calculates the average lead time for similar contracts when vendor, supplier, or account data exists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cm-contract-repository-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro AI agents, Contract Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Contract repository AI agent

This AI agent retrieves contract repository details for a specified record, including vendor information, contract model, and document attachment IDs. It also calculates the average lead time for similar contracts when vendor, supplier, or account data exists.

## Workflow

The agent retrieves contract repository details and starts metadata and obligation extraction for a specified record. It also initiates asynchronous extraction of key metadata from contract documents, such as effective dates, renewal and termination notice periods, and auto-renewal clauses.

1.  Retrieve the contract repository details for the specified record, including vendor, supplier, or account information, the contract model, and whether the obligations plugin is active.
2.  Start metadata extraction for the contract document, such as effective date, end date, and renewal and termination notice periods, without waiting for it to finish, and continue even if it encounters an error.
3.  If the obligations plugin is active, also start extraction of contractual obligations from the document without waiting for it to finish, and continue even if it encounters an error.
4.  If vendor, supplier, or account information is available, calculate the average lead time for similar contracts.
5.  Complete these steps automatically without asking the user for any input.

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

-   **Scripts**

Calculate average lead time of similar contracts

Get Contract repository details

Initiate metadata extraction

Initiate Obigation Extraction


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_cm\_gen\_ai.ai\_contract\_fulfiller

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sn\_lg\_ops.request\_fulfiller, sn\_cm\_core.contract\_fulfiller, contract\_manager, sn\_cm\_obligation.obligation\_fulfiller

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Renewal notice period remainder

</td></tr></tbody>
</table>For more information, see [Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-cmpro-landing-page.md).

**Parent Topic:**[Contract Management Pro AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/cm-ai-agents-overview.md)

