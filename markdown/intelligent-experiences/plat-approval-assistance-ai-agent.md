---
title: Approval assistance AI agent
description: This AI agent handles all queries related to approval records for the current user.This AI agent that enables you to see your list of pending approvals, as well as see the details about your pending approvals. You can then approve or reject requests and tickets in ServiceNow Otto for Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-approval-assistance-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 4
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
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

For more information, see [Using the approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-approval-assistance-ai-agent.md).

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

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

approver\_user, sn\_request\_approver\_read, snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

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

## Using the approval assistance AI agent

This AI agent that enables you to see your list of pending approvals, as well as see the details about your pending approvals. You can then approve or reject requests and tickets in ServiceNow Otto for Virtual Agent.

Roles required: approver\_user, sn\_request\_approver\_read, snc\_internal

**Note:** Add the necessary roles to enable reading of other tables whose records go through the approval process. For example, you can add the sn\_change\_read role to read Change Request records.

The benefit of using the approval assistance AI agent is that you don't need to navigate to a specific page to approve your tickets. You can ask the AI agent about your pending approval requests and then tell the AI agent to approve or reject those approvals. The AI agent will ask follow-up questions and offer context-aware responses to simplify your experience.

Ask you administrator to configure the display fields and the knowledge base \(KB\) search fields to generate a Gen AI checklist to assist the approval assistance AI agent in making targeted decisions. The checklist uses KB articles and policies to assist the agent in decision making. The checklist fetches information from knowledge base articles about specific requester approval tickets. An approval\_admin and admin role are required to configure the agent. For more information, see [Configure Service Portal Approval Configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-approval-assistance-ai-agent.md).

**Note:** Provide cross-scope privileges to the Requester Agents - Foundation plugin for tables whose records are restricted within the scope of an application. For more information, see [Define cross-scope access to an application resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/set-RCA-level.md).

### Prerequisites and setup

To use this AI agent, you must have Requester Agents - Foundation \(version 3 of the standard plugin\) installed on your instance, which is installed with ServiceNow Otto for Platform. You can get these plugins when you install any other ServiceNow Otto application, such as ServiceNow Otto for IT Service Management \(ITSM\).

The approval assistance AI agent displays data from the Approvals \[sysapproval\_approver\] table. If the user has been assigned to approve a request, the approval record is shown.

### Sample prompts

After the agent has been activated in AI Agent Studio, enter phrases such as the following or similar queries to run the AI agent in Virtual Agent and the ServiceNow Otto panel.

-   Can you give me a list of pending approvals?
-   What are the pending approvals for time off requests?
-   Show me a list of pending approval requests by priority.
-   Give me details about my approval request?

### Performing approval action on an approval record

The approval assistance AI agent shows approval requests that require an action on your part. After the approval information is provided by the agent, select **Approve** or **Reject** for a specific approval record, or type `Approve` or `Reject`. If you reject an approval request, then add a comment about the rejection reason.

\[Omitted image "aia-approve-reject.png"\] Alt text: Approve or Reject options for an approval.

