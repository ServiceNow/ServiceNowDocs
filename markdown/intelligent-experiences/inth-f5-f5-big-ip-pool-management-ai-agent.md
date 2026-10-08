---
title: F5 BIG-IP pool management AI agent
description: This AI agent manages F5 BIG-IP pools. It creates, checks, and deletes pools and adds, removes, enables, disables, and lists pool members.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-f5-f5-big-ip-pool-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [F5 BIG-IP Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# F5 BIG-IP pool management AI agent

This AI agent manages F5 BIG-IP pools. It creates, checks, and deletes pools and adds, removes, enables, disables, and lists pool members.

## Workflow

The agent helps the user manage load-balancing pools on F5 BIG-IP.

1.  Ask the user what they want to do and collect the details the action needs, such as the pool name and member details.
2.  Check a pool or list its members.
3.  Create a new pool.
4.  Add a member to a pool or remove one.
5.  Enable or disable a pool member.
6.  Delete a pool.
7.  Report the outcome to the user, including details of any error.

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

-   **Flow Actions**

Add Pool Member

Check Pool

Create Pool

Delete Pool

Disable Pool Member

Enable Pool Member

Get Pool Members

Remove Pool Member


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[F5 BIG-IP Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-f5-ai-agents-overview.md)

**Related topics**  


[F5 BIG-IP Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/f5-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

