---
title: GitHub repository management AI agent
description: This AI agent manages GitHub repositories and pull requests. It creates and deletes repositories, creates and merges pull requests, manages pull request comments, and looks up repositories, milestones, pull requests, and repository events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-github-github-repository-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [GitHub Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# GitHub repository management AI agent

This AI agent manages GitHub repositories and pull requests. It creates and deletes repositories, creates and merges pull requests, manages pull request comments, and looks up repositories, milestones, pull requests, and repository events.

## Workflow

The agent helps the user manage GitHub repositories and pull requests.

1.  Ask the user to describe the task.
2.  Ask the user for required inputs such as the repository owner, and use the user's own identity only when the user refers to themselves.
3.  Look up repositories, a repository's details, its milestones, or its events.
4.  Create a new repository or delete one.
5.  Look up pull requests, create a pull request, or merge one.
6.  Look up, update, reply to, or delete comments on a pull request.
7.  Report the outcome to the user, including details of any error.

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

-   **Flow Actions**

Create Pull Request

Create Reply on Pull Request Review Comment

Create Repository

Delete Comment on Pull Request

Delete Repository

Look up Comments on Pull Request Stream

Look up Milestones Stream

Look up Pull Requests Stream

Look up Repositories Stream

Look up Repository Details

Look up Repository Events Stream

Merge Pull Request

Update Comment on Pull Request


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[GitHub Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-github-ai-agents-overview.md)

**Related topics**  


[GitHub Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/github-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

