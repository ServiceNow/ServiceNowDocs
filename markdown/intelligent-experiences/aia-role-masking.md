---
title: Role masking in Now Assist AI agents
description: Role masking for AI agents and agentic workflows running as dynamic users enhances security by enabling users to limit the roles with which AI agents and agentic workflows execute, verifying that AI agents run with minimum necessary privileges.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 6
keywords: [Agent Role Masking, Agent Security]
breadcrumb: [Configuring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Role masking in Now Assist AI agents

Role masking for AI agents and agentic workflows running as dynamic users enhances security by enabling users to limit the roles with which AI agents and agentic workflows execute, verifying that AI agents run with minimum necessary privileges.

## Role masking overview

Role masking lets AI admins in the AI Agent Studio to limit permissions of agentic workflows or AI agents set tom run as dynamic users by defining an allow-list of roles they can inherit from invoking users, enforcing least-privilege access.

Use role masking to:

-   Empower users to follow least-access principles when an agentic workflow or AI agent executes on behalf of a dynamic user.
-   Limit roles that agentic workflows, AI agents, and skills inherit from users and can be applied when a user invokes them.

    For more information about configuring skills, see [Now Assist Skill Kit](../../now-assist-skill-kit/concept/now-assist-skill-kit-landing.md).

-   Reduce the risk of AI solutions accessing the resources that they shouldn't, therefore helping prevent agentic overreach into sensitive data or capabilities beyond what the user is allowed.
-   Expand the security configurations to increase functionality of agentic products while reducing security risks by enforcing governance for elevated or scoped roles.

## Prerequisites

To configure role masking on your ServiceNow instance, you must have:

-   Now Assist for Platform version 10.0.2-SS.
-   The sn\_aia.admin privileges.

## Role masking behavior

Role masking behavior in agentic workflows, AI agents, and tools controls which of the invoking user's roles are available to AI agents and tools during workflow execution. The roles are applied sequentially across layers in the agentic workflow, AI agent, and Tool sequence to verify that tools execute with minimum required privileges.

## Role masking rules

1.  Role masking limits the roles with which an agentic workflow, AI agent or Skill can execute to the intersection between the roles assigned to the invoking user and the riles included in the role masking approved roles list.
2.  AI user vs Role mask:

    The AI admin can choose for the component to run as either an AI user or a dynamic user. If set to run as a dynamic user, the AI admin can configure role masking for the component. Role masking cannot be configured for agentic workflows or AI agents set to run as AI users.

    -   If an AI user is selected, all roles assigned to the AI user are available to the agentic workflow or AI agent. This can be used to provide elevated access to the agentic workflow AI agent.

        **Note:** Tools always run as dynamic users.

    -   If Role masking is applied to an agentic workflow, AI agent, or tool running as a dynamic user, the component runs with roles with roles limited to the intersection of the current invoking user's roles and the roles included in the role masking approved roles list.
3.  Multiple role masks can be configured and applied in the agentic workflow - AI agent - tool sequence, but each mask still follows the intersection rule.
4.  Role masking only restricts roles that components can execute with, but never grants components roles which exceed those of the invoking user. Thus, if the invoking user has a role that is not included in the approved roles list, the component will not be allowed to execute with that role. And, if the approved roles list includes a role that is not assigned to the invoking user, the component will not be able to execute with that role again.
5.  When a workflow running as an AI user invokes an AI agent running as a dynamic user with role masking configured, then the roles available to the AI agent will be the intersection of the role masking configuration of the AI agent and the roles assigned to the AI user of the agentic workflow. The same holds true for an AI agent running as an AI user that then invokes a skill with role masking configured.

## ACL and role masking evaluation sequence

The following sequence defines how ACLs and role masks are evaluated across the agentic workflow, AI agent, and tool execution contexts:

-   **Step 1: Agentic workflow ACL validation**

    ACLs configured for workflows are evaluated against the invoking user \(automated or conversational\) session roles.

-   **Step 2: Agentic workflow role mask application**

    If the invoking user meets the agentic workflow's ACL criteria \(and the agentic workflow is set to run as a dynamic user with role masking configured\), the agentic workflow role masking is applied to the invoking user's roles \(there by restricting roles from the user session based on the intersection with the configured role masking\).

-   **Step 3: AI agent ACL validation**

    When an agentic workflow invokes an AI agent, the AI agents' ACLs are validated against one AI agent ACLs are validated against one of the roles with which the agentic workflow was approved to execute. Thus:

    -   If the agentic workflow was set to run as an AI user, the AI agent ACL will validate against the AI user session configured at the workflow.
    -   If the agentic workflow was set to run as a dynamic user with role masking, the AI agent ACL will check whether the effective remaining roles after applying the workflow role masking meets the ACL criteria.
-   **Step 4: AI agent role masking application**

    Similar to the agentic workflow above, either the AI user or the AI agent role mask is applied:

    -   If an AI user is selected, all roles of the AI user are enforced \(no masking\).
    -   If role mask is applied, then the roles are limited further based on intersection with the effective roles after applying the workflow role masking.
-   **Step 5: Tool ACL validation**

    If a tool uses ACLs, these are checked against the roles that the AI agent—assigned to the tool—is permitted to use. This means that if role masking is set up, only the roles left after masking are considered during validation.

-   **Step 6: Tool role masking application**

    If the tool is a skill and has role mask configured, then the approved roles will be applied to roles with which the AI agent was approved to run, thereby limiting roles for the tool's execution.


Summary of ACL and role masking evaluation order:

1.  **Agentic workflow ACLs** → validated with invoking \(conversational or automated\) user session's roles.
2.  **Agentic workflow role masking** → applied to the invoking user session.
3.  **AI agent ACLs** → validated with agentic workflow's approved roles \(agentic workflow's AI user OR roles after workflow role masking\).
4.  **AI agent role masking** → applied to agentic workflow's approved roles.
5.  **Tool ACLs** → validated with AI agent's approved roles \(AI agent's AI user or roles after agent role masking\).
6.  **Tool role mask \(Skills only\)** → applied to AI agent's approved roles.

**Note:** When evaluating ACLs and role masks, the admin can identify where and why execution failed due to either ACL or role mask restrictions.

## Configuration

-   To configure role masking for an AI agent, see [Define security controls for an AI agent](../task/define-sec-controls-aia.md).
-   To configure role masking for an AI agent, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

