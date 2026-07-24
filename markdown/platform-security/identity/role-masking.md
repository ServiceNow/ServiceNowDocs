---
title: Role masking for AI agents
description: Role masking for AI agents and agentic workflows helps administrators enhance security by limiting the roles those agents use during tool execution, and by verifying that AI agents run with least-access privileges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/role-masking.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 2
keywords: [role masking, AI agents, Agent Access Role Configuration, Agent Access Permission Set Configuration, least-access privileges, Allow all session roles]
breadcrumb: [Identity]
---

# Role masking for AI agents

Role masking for AI agents and agentic workflows helps administrators enhance security by limiting the roles those agents use during tool execution, and by verifying that AI agents run with least-access privileges.

An AI agent runs tools, queries data, and updates records on behalf of the user who triggered it. Without role masking, the agent inherits all of the triggering user's session roles, which can give the agent more access than its specialty requires.

Role masking lets you restrict the AI agent's runtime role set to only the roles needed for the agent's tools and tasks. By limiting the role set, you reduce the blast radius of any prompt-driven error or misuse, and you make the agent's behavior easier to audit.

## Role masking rules

1.  Role masking limits the roles with which an agentic workflow, AI agent or Skill can execute to the intersection between the roles assigned to the invoking user and the roles included in the role masking approved roles list.
2.  AI user vs Role mask:

    The AI admin can choose for the component to run as either an AI user or a dynamic user. If set to run as a dynamic user, the AI admin can configure role masking for the component. Role masking can't be configured for agentic workflows or AI agents set to run as AI users.

    -   If an AI user is selected, all roles assigned to the AI user are available to the agentic workflow or AI agent. This can be used to provide elevated access to the agentic workflow AI agent.

        **Note:** Tools run as dynamic users.

    -   If Role masking is applied to an agentic workflow, AI agent, or tool running as a dynamic user, the component runs with roles with roles limited to the intersection of the current invoking user's roles and the roles included in the role masking approved roles list.

To know more about AI agent role masking, see [Role masking in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md)

## Prerequisites

To configure role masking on your ServiceNow instance, you must have:

-   Now Assist for Platform version 10.0.2-SS.
-   The `sn_aia.admin` privileges.

## Dynamic role addition

You can add multiple roles to an AI agent's role masking configuration as individual records, rather than as a single delimited list. Each role you add through the embedded list on the **Agent Access Role Configuration** form creates a record in the **Agent access role** table.

This design supports the common case where different Business Units can use the same AI agent. The agent is shipped with a minimum set of roles, and each Business Unit can add the specific roles based on their use case. Since each role is a separate record in the table, Business Units can add and remove their own role entries independently, without affecting the role entries owned by other teams. To know more about the configuration, see .

