---
title: Create incident AI agent
description: Use this AI agent to log IT support requests. It responds to requests such as "create an incident," "raise an incident," "open an IT ticket," or "raise an IT support ticket."Use the AI agent incident creation workflow to report issues, review resolution plans, and automatically create incident records with duplicate detection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-create-incident-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI agent, incident creation, workflow]
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Create incident AI agent

Use this AI agent to log IT support requests. It responds to requests such as "create an incident," "raise an incident," "open an IT ticket," or "raise an IT support ticket."

## Workflow

bv

This agent first attempts to resolve the problem with self-service solutions. If the problem persists, it drafts a structured IT support incident, confirms the details with the user for accuracy, and creates the official record for tracking.

1.  Greet the user and gather information about the issue.
2.  Validate and clarify the user's issue.
3.  Create a search query based on the details gathered.
4.  Use the search query as input for the Show Self-Service Options tool. This conversational tool handles the entire self-service process.
5.  Evaluate the outcome. If the issue is solved, workflow is complete. If not, create an incident with the conversation history.
6.  Confirm the details with the user.
7.  Conclude the conversation based on the outcome.

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

-   **Conversational Topics**

Create Incident Record

Handle Similar Incidents

Show Self-Service Options


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

itil

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

Default VA Workflow

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

## Use the Create incident AI agent

Use the AI agent incident creation workflow to report issues, review resolution plans, and automatically create incident records with duplicate detection.

### Before you begin

Role required: none

**Note:** The AI agent executes the operations as an ITIL user.

### Procedure

1.  Open the Create Incident AI agent from one of the available contexts:

    -   ServiceNow Otto panel
    -   Employee Center
    -   ServiceNow Otto for Virtual Agent
2.  Describe the issue you're experiencing in the provided field.

    Provide details about the problem, including what you were trying to do, when the issue occurred, and any error messages or symptoms you observed.

3.  Submit your issue description to the agent.

    The agent analyzes your input and generates a proposed resolution plan based on the issue description and knowledge base.

4.  Review the resolution plan and select **Accept** or **Reject**.

    The agent displays a suggested resolution approach. If you accept the plan, the workflow proceeds to incident creation. If you reject it, you can provide additional guidance or take an alternative approach.

    \[Omitted image "itsm-create-incident-ai-agent-plan-review.png"\] Alt text: Resolution plan review screen showing Accept and Reject options

5.  Wait for the agent to check for similar existing incidents.

    **Note:** The similar incidents must have the following conditions:

    -   The incident must be active.
    -   The caller must be the logged-in user.
    -   The incident must have been created within the last 30 days.
    The agent queries the incident database to identify any duplicate or related incidents that might address the same issue. This duplicate detection helps prevent unnecessary incident creation and helps consolidate related issues.

6.  Review the incident created by the agent.

    If no duplicates are found, the agent creates a new incident record with all relevant information from your issue description. The incident is ready for assignment to the appropriate support team and includes a complete audit trail of the workflow.


### What to do next

Your incident is in the system and assigned to the appropriate team for investigation and resolution. Track the status through your ServiceNow portal or mobile app.

