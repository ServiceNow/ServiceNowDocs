---
title: Remediation tasks AI agent
description: This AI agent identifies the remediation tasks for resolving an issue by referencing the action plan field on the issue record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/grc-remediation-tasks-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance AI agents, Governance, Risk, and Compliance, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Remediation tasks AI agent

This AI agent identifies the remediation tasks for resolving an issue by referencing the action plan field on the issue record.

## Workflow

The agent helps users complete tasks related to remediation tasks.

1.  Fetch the sn\_grc\_issue sys\_id or number from the memory, or ask for the issue number.
2.  Use the Suggest remediation tasks for the issue tool to generate recommendations.
3.  Ask the user to accept, edit, or dismiss the suggestions.
4.  If the user chooses to edit the suggestions, refine them based on feedback.
5.  If the user accepts the suggestions, create the remediation tasks.
6.  End flow when tasks are complete or the user dismisses suggestions.

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

-   **Flow Action**

Create remediation task

-   **Generative AI skill**

Suggest remediation tasks for the issue


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_grc\_genai.issue\_aiagent\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_grc.business\_user, 90c5d097533320101d7dddeeff7b126e, sn\_grc.compliance\_assurance\_business\_user, sn\_grc\_genai.issue\_aiagent\_user, sn\_grc.user, snc\_required\_script\_writer\_permission

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

Optimize GRC issue resolution

</td></tr></tbody>
</table>For more information on Governance, Risk, and Compliance, see [Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

**Parent Topic:**[Governance, Risk, and Compliance AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/grc-ai-agents-overview.md)

