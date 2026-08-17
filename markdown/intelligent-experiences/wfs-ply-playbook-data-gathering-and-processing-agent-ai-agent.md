---
title: Playbook data gathering and processing AI agent
description: This ServiceNow Otto for Creator agent is a assistant that consolidates data gathering, processing, and slot-filling capabilities. It handles end-to-end playbook execution using a broad toolkit of retrieval, reasoning, and action-oriented functions. The agent also helps with tasks related to processing of files attached to instance records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wfs-ply-playbook-data-gathering-and-processing-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Playbook data gathering and processing AI agent

This ServiceNow Otto for Creator agent is a assistant that consolidates data gathering, processing, and slot-filling capabilities. It handles end-to-end playbook execution using a broad toolkit of retrieval, reasoning, and action-oriented functions. The agent also helps with tasks related to processing of files attached to instance records.

## Workflow

1.  Break the input into separate sub-objectives when it contains multiple distinct tasks; leave it as one task if it's already a single request.
2.  Run the appropriate retrieval method for each sub-objective \(search across records, structured knowledge lookups, knowledge article search, or web search\), including chaining steps together when a task requires first finding related records, then pulling specific details from them.
3.  For document/attachment requests, retrieve the attachment, generate a summary, and display it once complete.
4.  Apply operations like validation, summarization, classification, translation, or extraction when the task calls for transforming already-retrieved data.
5.  Merge all outputs into one response, or display "No results found" if the outcome is empty.

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

AI Search Data Retriever

Get results for QnA or Summarization task

Knowledge articles retriever tool

Knowledge Graph TextToResult API crawler

Retrieve attachments of a Glide record

Summarize attachments

-   **Web search**

Use web search


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

playbook\_agent\_user

</td></tr><tr><td>

Data access roles

</td><td>

Not defined.

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

Playbook Activity Assist

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Creator at [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator-landing.md).

**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

