---
title: MID keystore AI agent
description: This AI agent helps users diagnose and resolve MID Server keystore problems. This AI agent is designed for IT administrators who manage MID Server health.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-mid-mid-keystore-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [MID Server AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# MID keystore AI agent

This AI agent helps users diagnose and resolve MID Server keystore problems. This AI agent is designed for IT administrators who manage MID Server health.

## Workflow

The agent fetches MID Server and issue details, executes rekey and validation operations, provides step-by-step recovery instructions, and ensures the MID Server returns to a validated state.

1.  Identify the keystore issue from the user prompt or from the issue table.
2.  If the MID Server is up, walk the user through the rekeying process.
3.  If the MID Server is down, walk the user through troubleshooting steps.
4.  Validate the resolution.
5.  If the user verifies that the issue is resolved, end execution. Otherwise, restart the process.

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

Fetch a MID server details

Fetch keystore issues

MID script retriever

Rekey a MID server

Validate/Invalidate a MID server

-   **Subflows**

Verify rekey completion

Verify rekey trigger

Verify validation completion


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

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

MID Guardian

</td></tr></tbody>
</table>Learn more about MID Server management in [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-landing.md).

**Parent Topic:**[MID Server AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-mid-server-ai-agents-overview.md)

