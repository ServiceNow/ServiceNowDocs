---
title: Jira Service Management request management AI agent
description: This AI agent manages Jira Service Management customer requests. It creates requests and comments, performs transitions, manages participants and subscriptions, and looks up requests, comments, attachments, status history, and SLA information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-jira-sm-jira-service-management-request-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Jira Service Management Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Jira Service Management request management AI agent

This AI agent manages Jira Service Management customer requests. It creates requests and comments, performs transitions, manages participants and subscriptions, and looks up requests, comments, attachments, status history, and SLA information.

## Workflow

The agent helps the user create, track, and update customer requests in Jira Service Management.

1.  Ask the user what they want to do and collect the details the action needs, such as the request key or service desk.
2.  Look up customer requests, their comments and attachments, status history, or SLA information.
3.  Create a new customer request or add a comment to one, using temporary files or attachments where needed.
4.  Look up the available transitions for a request and perform a transition.
5.  Add participants to a request or remove them.
6.  Check, start, or stop the subscription to updates for a request.
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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Add Customer Request Participants

Create Customer Request

Create Customer Request Comment

Create Temporary Attachment

Create Temporary File

Look up Comment Attachment

Look up Customer Request Comments

Look up Customer Request Participants

Look up Customer Request Status History

Look up Customer Request Transitions

Look up Customer Requests

Look up SLA Information

Look up Subscription Status

Perform Customer Request Transition

Remove Customer Request Participants

Subscribe Customer Request

Unsubscribe Customer Request


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Jira Service Management Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-jira-sm-ai-agents-overview.md)

**Related topics**  


[Jira Service Management Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/jira-serv-mngmt.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md)

