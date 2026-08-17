---
title: Control objective change AI agent
description: This AI agent acts as a Compliance Manager that validates if the description and supplemental guidance of a given control objective need updates based on the associated citations. The AI agent recommends new values if changes are required, and updates the control objective record after getting confirmation from the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/grc-control-objective-change-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance AI agents, Governance, Risk, and Compliance, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Control objective change AI agent

This AI agent acts as a Compliance Manager that validates if the description and supplemental guidance of a given control objective need updates based on the associated citations. The AI agent recommends new values if changes are required, and updates the control objective record after getting confirmation from the user.

## Workflow

The agent helps users complete tasks related to control objective change agent.

1.  Greet the user and fetch the control objective based on the provided sys\_id.
2.  Review the control objective's description and supplemental guidance fields to determine if updates are needed.
3.  If the control objective is up to date, provide the user with an option for a manual update.
4.  If the control objective is requires an update, provide recommendations.
5.  Based on user's responses, update control objectives. Loop if necessary.
6.  Inquire about the next item. Loop until finished.
7.  Ending message.

For more information on Governance, Risk, and Compliance, see [Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

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

Fetch control objective details

Get list of impacted control objective

Mark control objective as reviewed

Update control objective details

-   **Generative AI skill**

Validate and recommend control objective field values


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_grc\_sharegenai.compliance\_library\_aiagent\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_compliance.manager, sn\_grc\_sharegenai.compliance\_library\_aiagent\_user

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
</table>For more information on Governance, Risk, and Compliance, see [Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)

**Parent Topic:**[Governance, Risk, and Compliance AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/grc-ai-agents-overview.md)

