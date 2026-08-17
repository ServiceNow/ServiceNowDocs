---
title: Content insights AI agent
description: This AI agent processes and analyazes content in the Content Understanding application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-content-insights-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Content Understanding AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Content insights AI agent

This AI agent processes and analyazes content in the Content Understanding application.

## Workflow

The agent has three main capabilities.

1.  Analyze the user's request and select the appropriate task:
    -   Extract specific fields from documents using predefined configurations.
    -   Analyze document content to answer specific user questions.
    -   Provide concise summaries of document content.
2.  Obtain the document either via user upload or a record number or sys\_id.
3.  Execute the task.
4.  Return results to the user.

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

-   **Search retrieval**

Get Relevant DocIntel Task Definition

-   **Subflow**

Submit and Fetch Results

-   **Scripts**

Get table name from record number

Retrieve attachments of a Glide record

Trigger Document Viewer Canvas

-   **Conversational topic**

Upload Document


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

platform\_ml\_di.creation\_agent, platform\_ml\_di.admin, platform\_ml\_di.manager

</td></tr><tr><td>

Data access roles

</td><td>

platform\_ml\_di.creation\_agent, platform\_ml\_di.admin, platform\_ml\_di.manager

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

-   Conversational Contract Search and Insights
-   Process images for new tasks
-   Generate carbon calculations for metrics

</td></tr></tbody>
</table>Learn more about Content understanding at [Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-landing.md).

**Parent Topic:**[Content Understanding AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-content-understanding-ai-agents-overview.md)

