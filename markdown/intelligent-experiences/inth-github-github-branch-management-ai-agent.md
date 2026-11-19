---
title: GitHub branch management AI agent
description: This AI agent manages GitHub branches. It lists a repository's branches and creates new branches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-github-github-branch-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [GitHub Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# GitHub branch management AI agent

This AI agent manages GitHub branches. It lists a repository's branches and creates new branches.

## Workflow

The agent helps the user review and create branches in a GitHub repository.

1.  Ask the user what they want to do and collect the details the action needs, such as the repository owner, repository name, and base branch.
2.  List the repository's branches.
3.  Create a new branch.
4.  Report the outcome to the user, including details of any error.

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

-   **Flow Actions**

Create Branch

Look up Branches Stream


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[GitHub Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-github-ai-agents-overview.md)

**Related topics**  


[GitHub Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/github-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md)

