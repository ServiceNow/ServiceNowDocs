---
title: Define security controls for an AI agent
description: In the guided setup for an AI agent, define security controls for who can access the AI agent and what data the AI agent has access to.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 3
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Define security controls for an AI agent

In the guided setup for an AI agent, define security controls for who can access the AI agent and what data the AI agent has access to.

## Before you begin

Role required: sn\_aia.admin

## About this task

The **Define security controls** step is divided into two parts: **Define user access** and **Define data access**. The former creates an ACL that determines who can discover or invoke the AI agent. The latter defines the data that the AI agent has access to once it’s invoked.

See [Security for AI agents](../concept/aia-security-implementation.md) for more information about creating ACLs and user identities for security for AI agent.

## Procedure

1.  Select which users can access the AI agent.

    The drop-down menu options are:

    -   Users with specified roles
    -   Authenticated users
    -   Public
    If you select **Users with specified roles**, you can select exactly which roles can access the AI agent.

    AI agents installed with Now Assist applications each require specific roles. To learn which roles they need, consult the documentation for the AI agent or the agentic workflow that uses the AI agent.

2.  Select **Save and continue** to move to the next step.

    Saving and moving onto the next step triggers the creation of an ACL for your AI agent. If you want to make changes later, you can return to the guided setup and change the options here. If you have the correct elevated role, you can also make edits directly on the ACL table.

    ![Define user access step for Approval Assistant agent](../image/def-user-access-aia.png)

3.  Define the user identity of the AI agent to determine what data it has access to.

    The two options are **Dynamic user** and **AI user**. The dynamic user is the user invoking the AI agent or the dynamic user of the agentic workflow calling on the AI agent. An AI user is a dedicated user that has its own specified roles that allow access, which could be more than the dynamic user.

    If you do not have an AI user but want to use the **AI user** identity, you need to create a new record on the User table. See [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAUser.md). Select **AI user** as the identity type.

    If you select **Dynamic user**, you can select the **Approved roles** that the AI agent runs with. By default, an AI agent runs as a dynamic user and has the roles of the invoking user. Select the approved roles to limit the data access that an AI agent could have. Role masking must be applied for all AI agents and agentic workflows to run as dynamic users.

    To override the role masking requirement for a specific agentic workflow or AI agent, admins with the correct elevated access can create an approved list of roles for a given agentic workflow or AI agent. Then, they can access that role masking record in the Agent Access Role Configurations table \[sys\_agent\_access\_role\_configuration\], and select the “allow all roles” check box. Taking these steps deactivates the requirement for a role masking approved roles list in AI Agent Studio, so the AI admin can return to AI Agent Studio and continue to configure the agentic workflow or AI agent without role masking applied.

    **Note:** Role masking should be applied as security best practice and adherence to the principle of least privilege. Overriding the role masking requirement isn’t recommended.

    If you select **AI user**, the list of roles that the AI user has is displayed.

    ![Define data access step for Approval Assistant agent](../image/def-data-access-aia.png)


## Result

You have created an ACL that determines who can discover and access your AI agent, and you have assigned a user identity \(and role masking, if relevant\) to the AI agent to determine what data it can access.

## What to do next

Select **Save and continue** to move to the next step, [Adding a trigger](add-trigger-aia.md). Adding a trigger is optional. You can also skip to the final step, [Select channels and access](channels-access-aia.md).

