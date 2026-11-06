---
title: Risk Suggestion AI agent
description: The Risk Suggestion AI agent builds context for an entity and suggests relevant risks for it. It draws on your internal risk library, model-driven inference, and, with your permission, external public sources, and then creates the confirmed risks as triage records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/grc-risk-suggestion-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance AI agents, Governance, Risk, and Compliance, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Risk Suggestion AI agent

The Risk Suggestion AI agent builds context for an entity and suggests relevant risks for it. It draws on your internal risk library, model-driven inference, and, with your permission, external public sources, and then creates the confirmed risks as triage records.

## Workflow

The agent helps the user identify potential risks for an entity and add them to the risk triage table.

1.  The agent retrieves and displays the entity's details, such as its name, description, class, location, and department.
2.  The agent asks which types of risks to focus on, such as IT, data privacy, operational sustainability, third-party, compliance, or operational risks. A follow-up question appears only when more information would change the risk assessment.
3.  The agent searches the internal risk library for relevant risk statements, generates additional model-inferred risks, and displays both lists.
4.  The agent asks whether to search external public sources for more risks and, if the user agrees, displays the external risks with their source URLs.
5.  The agent removes duplicates and risks that are already tracked for the entity, and displays the consolidated list of suggested risks.
6.  The user can rename risks, update descriptions, or remove risks from the list until the list is confirmed.
7.  The agent creates triage risk records for the confirmed risks and reports how many records were created.

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

-   **AI skill**

Generate model-inferred risks

Transform external risks in JSON format

-   **Script**

Create triage risk records

De-duplicate and categorize suggested risks

Get Entity Information

Search relevant risk statements

-   **Web search**

Search external risks


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user
-   sn\_risk.implementation\_manager
-   sn\_risk.manager

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

Suggest potential risks

</td></tr></tbody>
</table>For more information about AI capabilities in Risk Management, see [AI in Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-in-risk-management.md).

**Parent Topic:**[Governance, Risk, and Compliance AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/grc-ai-agents-overview.md)

