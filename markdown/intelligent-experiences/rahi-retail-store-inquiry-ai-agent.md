---
title: Store Inquiry AI Agent
description: The agent resolves retail store inquiries by finding the most relevant solution in similar cases, knowledge articles, and documents. It presents the best match with its source and, based on the user's choice, updates the case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/rahi-retail-store-inquiry-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Retail AI agents, Retail, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Store Inquiry AI Agent

The agent resolves retail store inquiries by finding the most relevant solution in similar cases, knowledge articles, and documents. It presents the best match with its source and, based on the user's choice, updates the case.

## Workflow

The agent helps the user resolve a retail store inquiry case by drafting a response from existing cases, knowledge articles, and documents.

1.  Retrieve the details of the current inquiry case.
2.  Search for similar cases and for knowledge articles related to the case short description. If neither returns results, tell the user that no suggestions are available.
3.  Extract an answer from the first related document found, if any.
4.  Review the content of the knowledge articles and similar cases that were found.
5.  Select the most relevant solution and present it with its source \(document, case, or knowledge article\) as a link.
6.  Ask the user to accept, edit, or reject the drafted response.
7.  Update the case based on the choice. If the user accepts or edits the response, resolve the case and add the response to the resolution notes. If the user rejects it, offer to add the response to the work notes.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Get Metadata

Get document list using comma separated list of 'Id' values

Get similar cases

Update record details

-   **Tool**

Get Case Details

Get relevant knowledge articles

Submit and Fetch Results


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_rtl\_stre\_servcs.agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_rtl\_stre\_servcs.agent

</td></tr><tr><td>

Triggers

</td><td>

The agent ships with the trigger StoreInquiryAgentTrigger. It fires when **Assigned to** is not empty and the case state changes from New to Open. It runs once, as the assigned user, in the Now Assist panel. The trigger is inactive by default.

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Retail at [Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-operations-overview.md).

**Parent Topic:**[Retail AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/retail-ai-agents-overview.md)

