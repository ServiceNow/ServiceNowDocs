---
title: Approval assistance AI agent
description: This AI agent handles all queries related to approval records for the current user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-approval-assistance-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Approval assistance AI agent

This AI agent handles all queries related to approval records for the current user.

## Workflow

The agent retrieves and filters pending approvals, provides detailed information about requested items, generates evaluation checklists based on knowledge base articles, and supports approval and rejection actions including e-signature management.

1.  Analyze the user’s message to identify what they are trying to do.
2.  Route the request directly to the step that matches the intended action:
    -   Retrieve all pending approvals assigned to the user, applying any filters specified by the user.
    -   Fetch full details for a specific approval record, always retrieving the most current data.
    -   Generate and display a checklist evaluation for the approval, grouping criteria by status and providing reference article links.
    -   Prompt the user to choose an approval action, handle e-signature requirements if applicable, and confirm the result of the action.

For more information, see [Platform Approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-approval-aia.md).

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

Approval Processor

Fetch approval record details

Get list of approvals

-   **Knowledge Graph**

Approval User Knowledge Graph

-   **Generative AI skill**

Checklist Generation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

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

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

