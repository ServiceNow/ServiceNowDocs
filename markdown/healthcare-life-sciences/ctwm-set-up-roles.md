---
title: Set up roles for Care Team Work Management users
description: Confirm that the appropriate roles are assigned to users of Care Team Work Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/ctwm-set-up-roles.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up roles and responsibilities, Configure, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up roles for Care Team Work Management users

Confirm that the appropriate roles are assigned to users of Care Team Work Management.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Work Management application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial setup process for healthcare organizations or at any time thereafter as needed.

**Example:** For a user to be able to run playbooks and create task templates, they should have the following role configuration:

1.  **sn\_cto.care\_team\_agent** or **sn\_cto.loc\_support\_agent** for access to the Care Team Work Management application.
2.  **sn\_hco\_orc.loc\_support\_agent** or **sn\_hco\_orc.admin** for access to forms from the Healthcare Orchestration plugin.
3.  **sn\_hco\_orc.plan\_author** for access to task plan creation, scheduling and the ability to select multiple organizations for playbooks.

For instructions on assigning roles to groups, see [Create a group for all care team members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-core/hco-create-team-members-group.md).

**Roles included with Care Team Work Management**

<table id="table_nhz_p3h_bgc"><tbody><tr><td>

**Role**

</td><td>

**Persona**

</td><td>

**Description**

</td></tr><tr><td>

**sn\_cto.care\_team\_agent**

</td><td>

Care Team Agent

</td><td>

Works on care team tasks and smart assessments.

</td></tr><tr><td>

**sn\_cto.care\_team\_agent\_manager**

</td><td>

Care Team Agent Manager

</td><td>

Configures addition/removal of care team members, task plan templates, and smart questionnaire templates.

</td></tr><tr><td>

**sn\_hco\_orc.plan\_author**

</td><td>

Operational Leader

</td><td>

The playbook plan author role that is required for a location support agent or an admin for them to be able to see the task plan template module and the playbook when they create a new task plan template.

</td></tr><tr><td>

**sn\_hco\_orc.loc\_support\_agent**

</td><td>

Support Agent

</td><td>

Creates and fulfill the Healthcare orchestration tasks. Can create healthcare orchestration cases.

</td></tr><tr><td>

**sn\_hco\_orc.loc\_support\_agent\_manager**

</td><td>

Support Agent Department Manager

</td><td>

Tracks and manages all the tasks and cases for support departments.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


