---
title: MID common AI agent
description: This AI agent helps users and support personnel to identify, analyze, and resolve MID Server issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-mid-mid-common-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [MID Server AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# MID common AI agent

This AI agent helps users and support personnel to identify, analyze, and resolve MID Server issues.

## Workflow

The agent retrieves data from error logs, collects necessary details from users, and provides actionable troubleshooting guidance sourced from official ServiceNow documentation.

1.  Search support.servicenow.com and the ServiceNow documentation site.
2.  Combine and summarize the results.
3.  Present the combined results in a clear format to user.
4.  Fetch MID Server errors and warnings if the user requests it.
5.  End workflow.

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

Fetch MID Server Details

Fetch the top errors/warnings/exception

Trigger log analysis tool

-   **Web searches**

Gather support information on site support.servicenow.com

Gather product documentation info from site www.servicenow.com/docs/

-   **Subflow**

Wait for log analysis to be executed


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_itom\_mid\_grdn.admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_itom\_mid\_grdn.admin

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

MID Guardian

</td></tr></tbody>
</table>Learn more about MID Server management in [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-landing.md).

**Parent Topic:**[MID Server AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-mid-server-ai-agents-overview.md)

