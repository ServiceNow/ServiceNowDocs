---
title: GitHub code automation AI agent
description: This AI agent acts as a coding partner for GitHub repositories. It clarifies requirements, proposes an approach, generates or updates code in context, and commits changes to a working branch and opens a pull request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-github-github-code-automation-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [GitHub Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# GitHub code automation AI agent

This AI agent acts as a coding partner for GitHub repositories. It clarifies requirements, proposes an approach, generates or updates code in context, and commits changes to a working branch and opens a pull request.

## Workflow

The agent helps the user plan, write, and commit code changes to a GitHub repository. The user must provide approval at each step.

1.  Clarify what the user wants to build or change, including the tech stack, and present a proposed architecture for the user to approve.
2.  Confirm the repository owner, repository name, and base branch, asking the user for any that are missing.
3.  List the repository's branches and let the user select an existing branch or create a new one from a base branch.
4.  Review the repository structure and the files related to the change.
5.  Generate or update each file, show the code to the user, and commit it to the working branch only after the user approves.
6.  Ask whether there are more changes to make and, when the user is done, offer to create a pull request.
7.  Create the pull request if requested and confirm completion with the user.

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

Create Branch

Create Pull Request

Create or update a File

Look up Branches

Look up File Content

Repository Schema Fetcher


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

