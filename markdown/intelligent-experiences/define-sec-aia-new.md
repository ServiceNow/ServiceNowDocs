---
title: Define access rules for an AI agent
description: Define security controls for an AI agent to determine which users can access it and what permissions they have.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/define-sec-aia-new.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 4
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Define access rules for an AI agent

Define security controls for an AI agent to determine which users can access it and what permissions they have.

## Before you begin

Role required: sn\_aia\_admin

## About this task

The Access rules section is divided into two parts: **Which users can access this AI agent \(ACLs\)** and **Which data this AI agent can access**. The former creates an ACL that determines who can discover or invoke the AI agent. The latter defines the data that the AI agent has access to once it's invoked.

See [Security for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md) for more information about creating ACLs and user identities for security for AI agents.

## Procedure

1.  Define user access by selecting an option from the **Allowed users** dropdown.

    The dropdown menu options are:

    -   Users with specified roles
    -   Authenticated users
    -   Public
    If you select **Users with specified roles**, you can select exactly which roles can access the AI agent.

    AI agents installed with AI applications each require specific roles. To learn which roles needed for AI agents associated with ServiceNow Otto applications, consult the documentation for the AI agent or the agentic workflow that uses the AI agent.

    Selecting **Public** means anyone who can reach the instance can invoke the agent. Use it only for agents that expose no record data. **Public** should be used sparingly.

    An access control list \(ACL\) is generated based on the roles you select. Saving triggers the creation of an ACL for your AI agent. If you want to make changes later, you can return to the guided setup and change the options here. If you have the correct elevated role, you can also make edits directly on the ACL table.

2.  Select whether third-party AI agents can access the AI agent.

    If selected, only AI agents with the correct user access can invoke the AI agent.

3.  Define data access by selecting a user identity type from the **Identity type** dropdown.

    The user identity determines what data the AI agent can read and write while it runs.

    The two options are **Dynamic user** and **AI user**. The dynamic user is the user invoking the AI agent or the dynamic user of the agentic workflow calling on the AI agent. An AI user is a dedicated user that has its own specified roles that allow access, which could be more than the dynamic user. Every invocation reads and writes with the AI user's roles regardless of who started it.

    If you do not have an AI user but want to use the **AI user** identity, you need to create a new record on the User table. See [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAUser.md). Select **AI user** as the identity type.

    If you select **Dynamic user**, you can select the **Approved roles** that the AI agent runs with. By default, an AI agent runs as a dynamic user and has the roles of the invoking user. Select the approved roles to limit the data access that an AI agent could have. Role filtering must be applied for all AI agents and agentic workflows to run as dynamic users. If you don't select any roles, the agent inherits whatever roles the invoking user holds.

    To override the role filtering requirement for a specific agentic workflow or AI agent, admins with the correct elevated access can create an approved list of roles for a given agentic workflow or AI agent. Then, they can access that role filtering record in the Agent Access Role Configurations table \[sys\_agent\_access\_role\_configuration\], and select the **allow all roles** check box. Taking these steps deactivates the requirement for a role filtering approved roles list in AI Agent Studio, so the AI admin can return to AI Agent Studio and continue to configure the agentic workflow or AI agent without role filtering applied.

    **Note:** Role filtering should be applied as security best practice and adherence to the principle of least privilege. Overriding the role filtering requirement isn't recommended.

    When testing an AI agent, run the AI agent with different roles to confirm that only the correct data is accessed for the user audience.

    \[Omitted image "ai-setup-sec-controls.png"\] Alt text: Security controls configuration for AI agents showing user access, data access, and third-party access settings.


## Result

You have created an ACL that determines who can discover and access your AI agent, and you have assigned a user identity \(and role filtering, if relevant\) to the AI agent to determine what data it can access.

## What to do next

Scroll down to the next section of the guided setup, **Triggers**, to [define specific conditions where the AI agent should run](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia-new.md). Adding triggers is optional.

