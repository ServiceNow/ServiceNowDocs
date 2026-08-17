---
title: Software entitlement allocation AI agent
description: This Software Asset Management agent allocates software licenses for a request item, handling device selection when required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sam-software-entitlement-allocation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Software Asset Management AI agents, Software Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Software entitlement allocation AI agent

This Software Asset Management agent allocates software licenses for a request item, handling device selection when required.

## Workflow

1.  Run the license allocation tool with the request item number. If it returns an error, stop immediately.
2.  If the allocation requires a device but none was found, prompt the user to select a device and re-run the allocation with the selected device. If no device is available, end.

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

-   **Conversational topic**

Get devices for a user topic

-   **Script**

License allocation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, itil, now\_assist\_panel\_user

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

Help manage software requests

</td></tr></tbody>
</table>Learn more about Software Asset Management at [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md).

**Parent Topic:**[Software Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sam-ai-agents-overview.md)

