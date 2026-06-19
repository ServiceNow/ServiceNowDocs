---
title: Role masking in Now Assist AI agents
description: Role masking for AI agents and agentic workflows helps users enhance security by enabling them to limit their roles during tool execution and verify that AI agents run with least-access privileges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/aia-role-masking.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 3
keywords: [Agent Role Masking, Agent Security]
breadcrumb: [Security for AI agents, Explore, Now Assist AI agents, Enable AI experiences]
---

# Role masking in Now Assist AI agents

Role masking for AI agents and agentic workflows helps users enhance security by enabling them to limit their roles during tool execution and verify that AI agents run with least-access privileges.

## Role masking overview

Role masking lets AI admins in the AI Agent Studio to limit permissions of agentic workflows or AI agents set to run as dynamic users by defining an allow-list of roles they can inherit from invoking users, enforcing least-privilege access.

Use role masking to:

-   Empower users to follow least-access principles when an agentic workflow or AI agent executes on behalf of a dynamic user.
-   Limit roles that agentic workflows, AI agents, and skills inherit from users and can be applied when a user invokes them.

    For more information about configuring skills, see [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

-   Reduce the risk of AI solutions accessing the resources that they shouldn't, therefore helping prevent agentic overreach into sensitive data or capabilities beyond what the user is allowed.
-   Expand the security configurations to increase functionality of agentic products while reducing security risks by enforcing governance for elevated or scoped roles.

## Prerequisites

To configure role masking on your ServiceNow instance, you must have:

-   Now Assist for Platform version 10.0.2-SS.
-   The sn\_aia.admin privileges.

## Role masking behavior

Role masking behavior in agentic workflows, AI agents, and tools controls which of the invoking user's roles are available to AI agents and tools during workflow execution. The roles are applied sequentially across layers in the agentic workflow, AI agent, and Tool sequence to verify that tools execute with minimum required privileges.

## Role masking rules

1.  Role masking limits the roles with which an agentic workflow, AI agent or Skill can execute to the intersection between the roles assigned to the invoking user and the roles included in the role masking approved roles list.
2.  AI user vs Role mask:

    The AI admin can choose for the component to run as either an AI user or a dynamic user. If set to run as a dynamic user, the AI admin can configure role masking for the component. Role masking cannot be configured for agentic workflows or AI agents set to run as AI users.

    -   If an AI user is selected, all roles assigned to the AI user are available to the agentic workflow or AI agent. This can be used to provide elevated access to the agentic workflow AI agent.

        **Note:** Tools always run as dynamic users.

    -   If Role masking is applied to an agentic workflow, AI agent, or tool running as a dynamic user, the component runs with roles with roles limited to the intersection of the current invoking user's roles and the roles included in the role masking approved roles list.
3.  Multiple role masks can be configured and applied in the agentic workflow - AI agent - tool sequence, but each mask still follows the intersection rule.
4.  Role masking only restricts roles that components can execute with, but never grants components roles which exceed those of the invoking user. Thus, if the invoking user has a role that is not included in the approved roles list, the component will not be allowed to execute with that role. And, if the approved roles list includes a role that is not assigned to the invoking user, the component will not be able to execute with that role again.
5.  When a workflow running as an AI user invokes an AI agent running as a dynamic user with role masking configured, then the roles available to the AI agent will be the intersection of the role masking configuration of the AI agent and the roles assigned to the AI user of the agentic workflow. The same holds true for an AI agent running as an AI user that then invokes a skill with role masking configured.

## Configuration

-   To configure role masking for an AI agent, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).
-   To configure role masking for an AI agent, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

