---
title: Report a GRC issue AI agent
description: This AI agent enriches the given issue description with additional information by looking at historical data and using GRC context. It analyzes, extracts key information \(such as issue type, date of occurrence, and so on\), and creates a GRC issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/grc-report-a-grc-issue-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance AI agents, Governance, Risk, and Compliance, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Report a GRC issue AI agent

This AI agent enriches the given issue description with additional information by looking at historical data and using GRC context. It analyzes, extracts key information \(such as issue type, date of occurrence, and so on\), and creates a GRC issue.

## Workflow

The agent helps users complete tasks related to report a GRC issue.

1.  Receive the user's request and gather key information.
2.  Review the isIssue field from the tool response and respond to the user.
3.  Ask the user for additional or missing issue details according to a template.
4.  Interact conversationally to refine the issue.
5.  Create an issue when the user is satisfied and selects **Submit**.

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

Create an issue

Issue related object information finder

-   **Generative AI skill**

Issue key information finder


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_grc\_genai.issue\_aiagent\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_grc.issue\_employee\_user, sn\_grc.business\_user, sn\_grc\_genai.issue\_aiagent\_user, 90c5d097533320101d7dddeeff7b126e, sn\_grc.compliance\_assurance\_business\_user

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

Default VA Workflow

</td></tr></tbody>
</table>For more information on Governance, Risk, and Compliance, see [Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

**Parent Topic:**[Governance, Risk, and Compliance AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/grc-ai-agents-overview.md)

