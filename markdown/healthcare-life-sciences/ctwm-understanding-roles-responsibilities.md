---
title: Setting up roles and responsibilities in Care Team Work Management
description: To manage access effectively in Care Team Work Management, first understand how roles and responsibilities work together. These concepts build on the Service Model Foundation \(SMF\) but are adapted for Healthcare Operations-specific use cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Setting up roles and responsibilities in Care Team Work Management

To manage access effectively in Care Team Work Management, first understand how roles and responsibilities work together. These concepts build on the Service Model Foundation \(SMF\) but are adapted for Healthcare Operations-specific use cases.

To understand how roles and responsibilities function in Healthcare Operations, see [Setting up roles and responsibilities for Healthcare Operations users](cto-setting-up-roles-responsibilities.md).

Roles control access to features, capabilities, and data in the Care Team Work Management application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial setup process for healthcare organizations or at any time thereafter as needed.

**Example:** For a user to be able to run playbooks and create task templates, they should have the following role configuration:

1.  **sn\_cto.care\_team\_agent** or **sn\_cto.loc\_support\_agent** for access to the Care Team Work Management application.
2.  **sn\_hco\_orc.loc\_support\_agent** or **sn\_hco\_orc.admin** for access to forms from the Healthcare Orchestration plugin.
3.  **sn\_hco\_orc.plan\_author** for access to task plan creation, scheduling and the ability to select multiple organizations for playbooks.

For instructions on assigning roles to groups, see [Create a group for all care team members in Healthcare Operations Core](../task/hco-create-team-members-group.md).

The following roles and responsibilities are included with Care Team Work Management.

<table id="table_zjz_lrn_khc"><thead><tr><th>

Role

</th><th>

Responsibility

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`sn_cto.care_team_agent`

</td><td>

Care Team AgentInherits Location Support Agent responsibility from Service Model Foundation.

</td><td>

Use the Care Team Agent responsibility to work on care team cases and care team tasks assigned to your healthcare organization\(s\).

</td></tr><tr><td>

`sn_cto.care_team_agent_manager`

</td><td>

Care Team Agent Manager or Operational LeaderInherits Location Manager Fulfiller role from Service Model Foundation.

</td><td>

Use the Care Team Agent Manager responsibility to work on care team cases and care team tasks assigned to your healthcare organizations, and manage your healthcare organization members.

</td></tr></tbody>
</table>