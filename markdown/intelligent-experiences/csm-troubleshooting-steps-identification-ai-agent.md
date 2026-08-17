---
title: Troubleshooting steps identification AI agent
description: An AI agent responsible for gathering required context, identifying troubleshooting steps by comparing with KBs, similar cases and standard operating manuals, and proposing additional troubleshooting steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-troubleshooting-steps-identification-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Troubleshooting steps identification AI agent

An AI agent responsible for gathering required context, identifying troubleshooting steps by comparing with KBs, similar cases and standard operating manuals, and proposing additional troubleshooting steps.

## Workflow

The agent helps users complete tasks related to troubleshooting steps identification.

1.  Retrieve case details and identify troubleshooting actions already attempted by the user to avoid duplication.
2.  Search for relevant troubleshooting guidance from similar cases and knowledge articles using the case description. If no relevant results are found, exit with the predefined message.
3.  Analyze retrieved cases and knowledge articles to extract actionable troubleshooting steps with correct source attribution.
4.  Identify and process any related documents linked to the search results, applying deterministic document selection logic and extracting troubleshooting steps when documents exist.
5.  Combine troubleshooting steps from cases, knowledge articles, and documents, then remove steps already attempted by the user or semantically equivalent duplicates.
6.  Present only unique, value-added troubleshooting recommendations in a structured format, clearly separating top recommendations, additional suggestions, and a fully hyperlinked sources section.
7.  Ask for confirmation before updating work notes, update them only upon approval, display the exact confirmation message when successful, and then exit the workflow.

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

Get case details using number and fields

Get document list using comma separated list of 'Id' values

Update the work notes of the case

-   **Subflows**

Get case details using number and fields

Submit and Fetch Results

-   **Search retrieval**

Get relevant knowledge articles

Get Similar Cases


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, platform\_ml\_di.creation\_agent

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

Not applicable.

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

