---
title: Configure role masking for an AI agent
description: Restrict the roles that an AI agent uses at runtime by creating an Agent Access Role Configuration record that limits the agent to a defined set of roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/configure-role-masking.html
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [role masking, AI agents, Agent Access Role Configuration, Agent Access Permission Set Configuration, Limit To Roles, Allow all session roles]
breadcrumb: [Role masking for AI agents, Identity]
---

# Configure role masking for an AI agent

Restrict the roles that an AI agent uses at runtime by creating an Agent Access Role Configuration record that limits the agent to a defined set of roles.

## Before you begin

Role required: `sn_aia.admin`

Before you configure role masking for an AI agent, the AI agent you need to restrict must already exist.

## Procedure

1.  Navigate to the **sys\_agent\_access\_configuration\_list.do** table.

    The Agent Access Role Configurations page opens.

2.  Select **New**.

    The **Agent Access Role Configuration - New Record** form opens.

3.  On the form, fill in the fields:

<table id="table_xxz_1jl_pjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the configuration. Example: `Action Designer role mask`.

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Description

</td><td>

Description of the configuration.

</td></tr><tr><td>

Agent Table

</td><td>

Table that holds the agent record you need to restrict.

</td></tr><tr><td>

Action

</td><td>

**Limit To Roles**. This action restricts the AI agent to the roles you add to the configuration. The agent can't use roles outside the selected roles.

</td></tr><tr><td>

Agent

</td><td>

The AI agent that the configuration applies to.

</td></tr><tr><td>

Role List

</td><td>

Roles to limit using the **Agent access roles** list. Each role added through this lookup is stored as an individual record in the Configuration table.**Note:**

-   Previously you could use role list to add the roles. You have to use the Agent access role table to add roles.
-   Existing records with the `role_list` column continues to operate as expected. All new role configurations are implemented through the `sys_agent_access_role_mapping` table.


</td></tr><tr><td>

Agent access role

</td><td>

Role selected using the **Insert a new row**. Each row you add creates one record in the Agent access roles table, linking the AI agent to that role.

</td></tr></tbody>
</table>    \[Omitted image "role-masking-configuration.png"\] Alt text: Agent Access Role Configuration

4.  Select **Submit**.


## Result

The platform saves each role masking entry in the Agent Access Role Configurations page. The next time the AI agent runs, it uses the roles that are mapped to an agent.

