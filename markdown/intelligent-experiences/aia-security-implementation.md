---
title: Implement access control in Now Assist AI agents
description: Implement security controls for AI agents and agentic workflows through access control lists \(ACLs\) and user identities to increase alignment with the access control-based security measures in the agentic system.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-09-11"
reading_time_minutes: 4
keywords: [Agentic AI Security, ACLs in AI agents]
breadcrumb: [Explore, Now Assist AI agents, Enable AI experiences]
---

# Implement access control in Now Assist AI agents

Implement security controls for AI agents and agentic workflows through access control lists \(ACLs\) and user identities to increase alignment with the access control-based security measures in the agentic system.

## Security for AI agents overview

Access controls for agentic AI on the ServiceNow AI Platform comprises two major components: Access control lists \(ACLs\) and user identities. The interaction between these two components at the agentic workflow, AI agent, and tool levels within the AI Agent Studio influences their overall security and functionality.

## Access control lists

The access control lists \(ACLs\) in Now Assist AI agents determine users who can invoke an agentic workflow or an AI agent. ACLs must be configured individually for each agentic workflow, AI agent, and certain AI agent tools.

The ACLs added to an AI agent and agentic workflow are available in the respective related lists for reference.

**Important:** ACLs configured in AI Agent Studio only determine the roles required for users to invoke an agentic workflow or an AI agent. They don't determine the access that the agentic workflow or an AI agent has once it’s invoked.

## User identity

The user identity determines the roles that the AI agent or an agentic workflow operates with and the data it can access depending on the permissions assigned to the .

After configuring the access control lists \(ACLs\), you must configure the User identity \(also called as **Run as**\) using which the AI agent or agentic workflow gets executed. There are two possible user configurations to select from:

-   **Dynamic user**: The logged-in user who invokes the execution of an AI agent or an agentic workflow. Dynamic user is the default user identity, and you can use the dynamic user unless there's a specific need that justifies an AI user.
-   **AI user**: A dedicated user who executes the AI agent or an agentic workflow with assigned roles that remain consistent regardless of who or how the execution is invoked. For example, an AI agent or an agentic workflow may need to be run with elevated privileges that the dynamic user might not have.

If you do not have an AI user but want to use the **AI user** identity, you need to create a new record on the User table. See [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAUser.md). Select **AI user** as the identity type.

**Note:**

-   An AI user can be configured as part of user identity and user identities are configured at the agentic workflow and AI agent levels.
    -   For more information about user identity in an AI agent, refer to [Create an AI agent](../task/configure-next-best-action-agent.md).
    -   For more information about user identity in an agentic workflow, refer to [Create an agentic workflow](../task/configure-use-case-ai-agents.md).
-   The ACLs are checked with the actual conversational user, a user who has invoked the agentic workflow or the AI agent. Once the ACL check is complete, the user identities can be applied.

## Configure ACLs in AI Agent Studio

ACLs configured in the AI Agent Studio for AI agents and agentic workflows are role-based and are of two types:

-   **Allow-If**: Grants access to data or resources when all the specified conditions in the ACL are met and the ACL doesn't prevent other ACLs from granting access to the same resource even if it doesn't.
-   **Deny-Unless**: Grants access only when the roles meet a specified condition and no other ACLs can override or grant access to that resource.

There are three possible options for ACLs created in AI Agent Studio:

-   **Any authenticated user**: Grants access to any user who is authenticated on the instance, regardless of the role.
-   **Users with specified roles**: The default ACL option that requires you to select the roles to invoke an AI agent or an agentic workflow.
-   **Public**: Grants access to all users, including guests who aren’t signed in.

Each AI agent and agentic workflow must have its own unique ACL.

-   To configure an ACL in the AI Agent Studio for an AI agent, see the [Create an AI agent](../task/configure-next-best-action-agent.md) guided setup.
-   To configure an ACL for an agentic workflow, see the [Create an agentic workflow](../task/configure-use-case-ai-agents.md) guided setup.

**Note:** If there are conflicting security requirements between agentic workflows, AI agents, and AI agent tools, or if the invoking user meets the criteria for some ACLs but not others, your agentic AI fails to execute. When configuring these security settings, consider all aspects of the agentic system- including the agentic workflow, AI agents, and tools.

## Supervised execution mode for AI agents

You can minimize potential negative impact of an AI agent not executing as expected by configuring AI agents' tools to run in supervised mode. This will ensure human oversight for the tool's actions. You can use the Supervised mode to enhance security for agents with the capability to perform sensitive or critical actions.

You can set the supervised execution mode when creating a tool in the AI agent guided setup. For example, choose Supervised as the Execution mode when adding a catalog item tool. For reference, see [Add a catalog item to an AI agent](../task/add-catalog-ai-agent.md).

