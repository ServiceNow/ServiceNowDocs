---
title: Change CI suggestion AI agent \(latest\)
description: This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change request without requiring multiple user interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/change-ai-orch-ci-suggestion-ai-agent.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Change CI suggestion AI agent \(latest\)

This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change request without requiring multiple user interactions.

**Note:** Available starting with the Zurich Patch 12 release. Requires ServiceNow Otto for IT Service Management \(ITSM\) v17.1.2 or later.

## Workflow

1.  Get the current Change Request number from the active change record or from the use input.
2.  Retrieve the change request context from its field values.
3.  Analyze the change details to identify the Primary CI and Affected CI candidates.
4.  Present the candidate CIs list to user for identifying a suitable Primary CI or Affected CIs.
5.  Automatically update the change request record with the user-selected primary CI and affected CIs.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Get context

Get configuration items for change

Get configuration items for change based on user input

Associate configuration items to change

Check primary CI on change

Update primary CI on change


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

itil, sn\_change\_write, cmdb\_readThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

itil, sn\_change\_write, cmdb\_readThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>