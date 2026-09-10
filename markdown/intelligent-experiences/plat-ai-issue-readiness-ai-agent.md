---
title: Issue readiness AI agent
description: This AI agent scans the record fields and context of a ticket so it can determine if it is ready for a fulfiller to work on it.This AI agent analyzes a record's information, determines whether all relevant information is present on the record, and then makes a decision about whether the task is ready for work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-issue-readiness-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 4
keywords: [task readiness]
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
---

# Issue readiness AI agent

This AI agent scans the record fields and context of a ticket so it can determine if it is ready for a fulfiller to work on it.

## Workflow

1.  Retrieve the record details, such as short description, description, activity stream, emails, approval, table name, and similar records.
2.  Analyze task details, focusing on information added by fulfillers.
3.  Analyze similar records.
4.  If any of the following are true, mark the task as NOT READY:
    -   A request or question \(from a fulfiller\) is detected and no clear response or resolution is found in the task record.
    -   The approval field's value is "requested" \(case-insensitive\). \(Values such as "not yet requested" or "not requested" don't block readiness.\)
    -   The task lacks information that is consistently present in similar records \(if available\) for the same type of request, and that missing information is relevant to fulfill the request \(for example, missing steps, confirmations, or outcome\).
    -   The overall quality or clarity of the task data is poor, such as unclear context that would reasonably block progress.

For more information, see [Using the issue readiness AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-ai-issue-readiness-ai-agent.md).

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

Create or update the record status

Get the record data


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_issue\_readiness

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_issue\_readiness, sn\_uxc\_gen\_ai.platform\_ai\_record\_mgmt

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

## Using the issue readiness AI agent

This AI agent analyzes a record's information, determines whether all relevant information is present on the record, and then makes a decision about whether the task is ready for work.

### Issue Readiness AI agent overview

Using the AI agent can help fulfillers focus on actionable work by reducing manual checks for missing supporting details or back-and-forth conversations. Instead of having to check whether tasks are waiting on pending approvals or unanswered questions, fulfillers can see what actionable work is available and prioritize it.

### Prerequisites and setup

To use this AI agent, you must have the Requester Agents - Foundation plugin installed on your instance, which is installed with any other ServiceNow Otto application, such as ServiceNow Otto for IT Service Management \(ITSM\).

### Testing the Issue Readiness AI agent

You can manually test the AI agent execution on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md). Select the AI agent, start a manual test, and use utterances in the Task field like the ones below.

### Sample prompts

After the agent has been activated in AI Agent Studio, enter phrases such as the following or similar queries to run the AI agent in Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.

-   Is INC001234 ready for work?
-   Do I have enough details on CSM0001234 to start?

