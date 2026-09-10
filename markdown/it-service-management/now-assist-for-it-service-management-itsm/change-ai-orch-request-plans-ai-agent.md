---
title: Change request plans AI agent \(autonomous\)
description: This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/change-ai-orch-request-plans-ai-agent.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Change Management, Use agentic AI in IT Service Management, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Change request plans AI agent \(autonomous\)

This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.

## Workflow

1.  Autonomously retrieve the change request record and all available change policy documents.
2.  Resolve the applicable change policy by matching the change model field \(chg\_model\) against available policy definitions.
3.  If no policy matches on change model, autonomously fall back to matching the change type field \(chg\_type\) against policy definitions.
4.  Determine whether a policy document is available for the resolved policy.
5.  If a policy document is available, autonomously identify the plan fields defined in the POLICY\_EXTRACTION\_KEYS schema.
6.  Populate only the identified plan fields with content generated based on the policy requirements.
7.  If no policy document is available, autonomously apply default field-population logic to draft all plan fields: Implementation plan, Backout plan, Test plan, Justification, and Risk and impact analysis.
8.  Update the change request with populated plan fields and return confirmation to the user in a single message.

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

Generate Change request Plans

Get All Change Request Data

Get Change Quality Policy Document

Get current change request details

Update plans to change request


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

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

Not applicable.

</td></tr></tbody>
</table>