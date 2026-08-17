---
title: Evaluate asset AI agent
description: This AI agent assists users in troubleshooting asset-related issues by using the Web Search tool, guiding them to select an appropriate resolution, and automatically completing the troubleshooting task upon confirmation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itam-evaluate-asset-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Asset Management AI agents, IT Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Evaluate asset AI agent

This AI agent assists users in troubleshooting asset-related issues by using the Web Search tool, guiding them to select an appropriate resolution, and automatically completing the troubleshooting task upon confirmation.

## Workflow

The agent helps users troubleshoot asset-related issues.

1.  Perform a web search and create a step by step hardware evaluation plan from the official &lt;asset\_manufacturer&gt; website for &lt;asset\_model&gt;. Provide warranty consideration guidelines and void-prevention measures for different inspection scenarios. Give detailed steps for each issue.
2.  Refine and format search results.
3.  Display numbered troubleshooting steps to the user, one at a time.
4.  If the user indicates that the problem is solved, end the workflow.
5.  If the user indicates that the problem is not solved, go to the next troubleshooting step.
6.  When all steps are exhausted, end the workflow.

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

-   **Conversational Topic**

Repair Order - Troubleshooting result

-   **Web search**

Use web search


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

inventory\_user

</td></tr><tr><td>

Data access roles

</td><td>

inventory\_user, 8c5ce94b77ac4210fa3fca22fe5a994b

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

-   Help repair hardware assets
-   Help repair enterprise assets

</td></tr></tbody>
</table>Learn more about IT Asset Management at .

**Parent Topic:**[IT Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itam-ai-agents-overview.md)

