---
title: Issue action plan AI agent
description: This AI agent identifies the optimal steps for resolving an issue by referencing the past similar issue details. It presents a step-by-step summarized action plan to the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/grc-issue-action-plan-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance AI agents, Governance, Risk, and Compliance, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Issue action plan AI agent

This AI agent identifies the optimal steps for resolving an issue by referencing the past similar issue details. It presents a step-by-step summarized action plan to the user.

## Workflow

The agent helps users complete tasks related to issue action plan.

1.  Get record details.
2.  Generate an action plan for the issue using the Generate Issue Action Plan tool.
3.  Ask for user feedback.
4.  If the user chooses to dismiss the action plan, inform the user that they can populate the action plan manually.
5.  If the user chooses to edit the action plan, show a message asking for the user’s feedback to refine the action plan.
6.  Use user feedback to refine the action plan.
7.  If the user chooses to accept the action plan, format and save it.

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

-   **Generative AI skill**

Generate Issue Action Plan

-   **Record Operations**

Get Issue Detail

Issue Resolution Agent Usage Status column Update Tool

Save action plan


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

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Optimize GRC issue resolution

</td></tr></tbody>
</table>For more information on Governance, Risk, and Compliance, see [Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

**Parent Topic:**[Governance, Risk, and Compliance AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/grc-ai-agents-overview.md)

