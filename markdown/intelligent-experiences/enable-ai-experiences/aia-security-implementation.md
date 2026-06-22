---
title: Implement access control in Now Assist AI agents
description: Implement security controls for AI agents and agentic workflows through access control lists \(ACLs\), user identities, and role masking to implement the access control-based security measures in the agentic system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/aia-security-implementation.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-09-11"
reading_time_minutes: 4
keywords: [agentic AI Security, ACLs in AI agents]
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Implement access control in Now Assist AI agents

Implement security controls for AI agents and agentic workflows through access control lists \(ACLs\), user identities, and role masking to implement the access control-based security measures in the agentic system.

## Security for AI agents overview

Access controls for agentic AI on the ServiceNow AI Platform comprises the major aspects: determining which users can access agentic AI resources, and what access each of those resources has once invoked. These aspects are controlled through three main components: access control lists \(ACLs\), user identities and role masking. The interaction between these components at the agentic workflow, AI agent, and tool levels within the AI Agent Studio influences their overall security and functionality.

## Access control lists

The access control lists \(ACLs\) in Now Assist AI agents determine which role\(s\) a user must have to be allowed to invoke an agentic workflow or an AI agent. ACLs must be configured individually for each agentic workflow, AI agent, and certain AI agent tools.

The ACLs added to an AI agent and agentic workflow are available in the respective related lists for reference.

**Important:** ACLs configured in AI Agent Studio only determine the roles required for users to invoke an agentic workflow or an AI agent. They don't determine the access that the agentic workflow or an AI agent has once it’s invoked.

## User identity

The user identity determines which user the AI agent or an agentic workflow operates as during execution, and therefore the data it can access and the actions it can take, depending on the roles assigned to the user identity.

After configuring the access control lists \(ACLs\), you must configure the User identity \(also called as **Run as**\) which the AI agent or agentic workflow will run as during execution.

**Note:** Each agentic workflow and AI agent has its own user identity configuration.

There are two possible user configurations to select from:

-   **Dynamic user**: The user identity of the person or resource \(automated trigger/agentic workflow/parent agent\) invokes the execution of an AI agent or an agentic workflow. The roles assigned to the agentic workflow or AI agent will change dynamically depending on the identity of the invoking user.

    **Note:** Dynamic user is the default user identity, and you can use the dynamic user unless there's a specific need that justifies an AI user.

-   **AI user**: A dedicated user identity that the AI agent or an agentic workflow runs as during execution, which has assigned roles that remain consistent regardless of who or how the execution is invoked. For example, an AI agent or an agentic workflow may need to be run with elevated privileges that the dynamic user might not have. If configured as a dynamic user, the execution would fail. However, if the AI agent or agentic workflow is configured to run as an AI user that has the elevated roles assigned to it, the execution will succeed even when invoked by a user with lower privileges.

If you don't have a suitable AI user but want to use the **AI user** identity, you must create a record on the User \[sys\_user\] table. See [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/t_CreateAUser.md) and select **AI user** as the identity type.

**Note:**

-   Role masking limits which roles an AI agent can use during execution. It only applies when the agent runs as a dynamic user — not when it runs as an AI user. The key difference: AI users determine the identity the agent runs as and role masking narrows the roles available to an agent that run as a dynamic user.
    -   For more information about user identity in an AI agent, refer to [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).
    -   For more information about user identity in an agentic workflow, refer to [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).
-   For each component’s execution, the ACL is checked against the invoking user identity, and if passed, the component’s run as user identity is applied. Any downstream components’ ACLs are checked in comparison to the run as user identity of component directly before it in the agentic hierarchy, and their run as user identities are passed down to the next downstream component’s ACLs.

    **Note:**

    -   Now Assist Skills and other tools of AI agents always run as Dynamic Users.
    -   This flow applies to user-invoked agents. Agents with automated triggers operate without a conversational user; role masking still applies, but the invoking context is a system session rather than an individual user.

## Supervised execution mode for AI agents

Configuring AI agents' tools to run in supervised mode is another way to minimize the potential negative impact of an AI agent that is not executing as expected. This will require human approval for the tool's actions before it executes. You can use the Supervised mode to enhance security for agents with the capability to perform sensitive or critical actions.

You can set the supervised execution mode when creating a tool in the AI agent guided setup. For example, choose Supervised as the Execution mode when adding a catalog item tool. For reference, see [Add a catalog item to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/add-catalog-ai-agent.md).

