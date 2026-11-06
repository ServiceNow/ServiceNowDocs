---
title: Plan and execute recall campaign phases AI agent
description: The Plan and execute recall campaign phases and subphases AI agent helps users create and modify phased rollouts for recall campaigns. Using the dimensions available in the Knowledge Graph schema, it gathers requirements, generates phase plans, and creates the phases for the plan that the user selects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mco-plan-and-execute-recall-campaign-phases-and-subphases-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Manufacturing Commercial Operations AI agents, Manufacturing Commercial Operations, AI agents library, AI assets, Enable AI experiences]
---

# Plan and execute recall campaign phases AI agent

The Plan and execute recall campaign phases and subphases AI agent helps users create and modify phased rollouts for recall campaigns. Using the dimensions available in the Knowledge Graph schema, it gathers requirements, generates phase plans, and creates the phases for the plan that the user selects.

## Workflow

The agent helps the user plan a phased rollout for an in-progress recall campaign and create the phases in the system.

1.  Show the in-progress recall campaigns and ask the user to select one.
2.  Display any existing phases on the campaign and ask whether to cancel draft phases so that their impacted assets can be included in phase planning.
3.  Show existing phase plans for the campaign to modify, or start a new plan if none exist.
4.  Ask the user to describe the phase requirements, and suggest dimensions from the Knowledge Graph schema if the user needs help.
5.  Map the requirements to available schema dimensions, flag any that can't be mapped, and confirm the understanding with the user.
6.  Generate phase plans and display them for the user to choose from.
7.  Confirm the selected plan, or regenerate plans if the user wants changes.
8.  Create the phases on the recall campaign, summarize the result, and offer to plan phases for another campaign.

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

-   **Script**

Fetch all inprogress recall campaigns

Generate phase plans

Generate phases from a phase plan

Phase plan HTML generator

Retrieve Knowledge Graph Schema

Retrieve phase hierarchy for already present phases on recall campaign


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_rcl\_claim\_mgmt.recall\_manager

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_rcl\_claim\_mgmt.recall\_manager

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

Execute recall campaigns faster

</td></tr></tbody>
</table>Learn more about Manufacturing Commercial Operations at [Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-overview.md).

