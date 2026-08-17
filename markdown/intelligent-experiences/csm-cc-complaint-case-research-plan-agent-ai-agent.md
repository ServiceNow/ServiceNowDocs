---
title: Complaint case research plan AI agent
description: Analyzes "Under Review" complaint cases to identify previously attempted troubleshooting steps and recommends new solutions from similar closed cases and knowledge articles. Prioritizes relevant suggestions, presents them with source attribution, updates work notes, and creates case task plans based on successful resolution patterns. Filters redundant recommendations and ensures proper workflow integration within case management systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-cc-complaint-case-research-plan-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Complaint case research plan AI agent

Analyzes "Under Review" complaint cases to identify previously attempted troubleshooting steps and recommends new solutions from similar closed cases and knowledge articles. Prioritizes relevant suggestions, presents them with source attribution, updates work notes, and creates case task plans based on successful resolution patterns. Filters redundant recommendations and ensures proper workflow integration within case management systems.

## Workflow

The agent helps users complete tasks related to complaint case research plan agent.

1.  Retrieve case details.
2.  Display previously attempted troubleshooting steps, if applicable.
3.  Search for similar cases and knowledge articles.
4.  Analyze troubleshooting steps and similar cases.
5.  Generate a list of unique troubleshooting steps and present it to the customer, including links to sources.
6.  Ask customer if they want to add these case tasks to the case.
7.  Confirm with user and end the process.

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

-   **Script**

Create case tasks

Get case details using number and fields

Get case task details

Update worknotes

-   **Search retrieval**

Get Similar complaint cases and Relevant knowledge articles


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

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

Accelerate Complaint Case Handling

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

