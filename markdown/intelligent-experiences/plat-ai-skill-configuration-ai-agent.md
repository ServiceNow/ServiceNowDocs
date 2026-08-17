---
title: Skill configuration AI agent
description: This AI agent executes all configuration operations for generative AI skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-skill-configuration-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Skill configuration AI agent

This AI agent executes all configuration operations for generative AI skills.

## Workflow

The agent operates as a child agent in autonomous mode. It does not ask for user confirmation.

This agent can perform the following tasks:

-   Validate all prerequisite conditions before operations \(generic and skill-specific validations\).
-   Execute skill activation and deactivation operations.
-   Provide detailed validation failure reports with actionable resolution guidance.
-   Return comprehensive operation results with clear success or failure indicators.
-   Handle errors gracefully and providing meaningful error messages.
-   Update ACL role assignments for generative AI skills using the Update Skill Roles tool.

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

Execute Skill Operation

Update Skill Roles


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_na\_center.nac\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_na\_center.nac\_admin

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

Skill Management Workflow

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

