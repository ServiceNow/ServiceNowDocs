---
title: Complaint case triage AI agent
description: This agent is designed to analyze complaint cases after their creation, automatically deriving key classification and prioritization fields. It serves case handlers and support teams by providing reliable, data-driven insights to enhance case management efficiency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-cc-complaint-case-triage-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Complaint case triage AI agent

This agent is designed to analyze complaint cases after their creation, automatically deriving key classification and prioritization fields. It serves case handlers and support teams by providing reliable, data-driven insights to enhance case management efficiency.

## Workflow

The agent helps users complete tasks related to complaint case triage agent.

1.  Filter the categories to only show those that correspond to the case's complaint\_type value.
2.  The subcategory value must correspond to the selected category value.
3.  Examine the output fields returned by the "Get case details using number and fields" tool and use this data to identify the category and subcategory.

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

Category and subcategory choices

Get case details using number and fields

Update fields

Update worknotes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_customerservice.consumer\_agent, sn\_customerservice\_agent

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

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Accelerate Complaint Case Handling

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

