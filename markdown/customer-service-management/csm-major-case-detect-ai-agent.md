---
title: Major case detect AI agent
description: This agent detects major case candidates by searching for cases similar to a newly created case, and either links the case to an existing major case or proposes it as a new major case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-major-case-detect-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-21"
reading_time_minutes: 2
breadcrumb: [Configure ServiceNow Otto for CSM Major Issue Management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Major case detect AI agent

This agent detects major case candidates by searching for cases similar to a newly created case, and either links the case to an existing major case or proposes it as a new major case.

## Workflow

The agent runs when a case is created that matches its trigger condition.

1.  Get the triggering case's details, including its major case state, parent case, and a combined search query built from its short description, description, and recent comments.
2.  Search for cases similar to the triggering case. The agent first searches existing accepted or proposed major cases; if none match, it falls back to searching open non-major cases.
3.  Decide whether to link the case to an existing major case or, if enough similar non-major cases are found, propose the case as a new major case.
4.  Update the case: set `suggested_major_case` and `business_impact`, and add a work note with the AI-generated reasoning.

**Note:** The trigger that starts this agent is shipped **inactive**. An administrator must activate it before the agent runs on any case.

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

-   **Script tool**

Get Case Details – retrieves the case number, major case state, parent case, and a combined search query for the triggering case.

-   **Script tool**

Detect Similar Cases – performs a semantic similarity search for cases similar to the triggering case.

-   **Script tool**

Update Major Case Suggestion – updates the case with the major case link or proposal and writes the AI-generated work note.


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_majorissue\_mgt.major\_issue\_manager

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_majorissue\_mgt.major\_issue\_manager

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

 Fires when a case is created with priority 1 or 2, no parent case, and a major case state that is not already proposed or accepted.

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Detect and link major case candidates during major issue management

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_CustomerServiceManagement.md). For the configurable detection thresholds this agent uses, see [Configure ServiceNow Otto for CSM Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-na-for-csm-major-issue-management.md).

