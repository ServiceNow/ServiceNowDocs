---
title: Transfer legal request AI agent
description: This AI agent transfers a legal request to the predicted category.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/lsd-transfer-legal-request-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Legal Service Delivery AI agents, Legal Service Delivery, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Transfer legal request AI agent

This AI agent transfers a legal request to the predicted category.

## Workflow

The agent helps users complete tasks related to transfer legal request.

1.  Use the Transfer legal request tool to transfer the legal request to the predicted category.
2.  End the current conversation.

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

Transfer legal request


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_lg\_ops.request\_fulfiller

</td></tr><tr><td>

Data access roles

</td><td>

sn\_lg\_ops.request\_fulfiller

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

Triage legal requests

</td></tr></tbody>
</table>Learn more about Legal Service Delivery at [Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-management-overview.md).

**Parent Topic:**[Legal Service Delivery AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/lsd-ai-agents-overview.md)

