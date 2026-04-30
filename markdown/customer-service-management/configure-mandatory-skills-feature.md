---
title: Configuring Mandatory Skills
description: Configure the mandatory skills feature for use with the Customer Service Management and Field Service Management applications.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mandatory Skills, Configure skills management, Configure case routing and assignment, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configuring Mandatory Skills

Configure the mandatory skills feature for use with the Customer Service Management and Field Service Management applications.

Mandatory skills are an optional feature included with the Customer Service Management and Field Service Management plugins. Use the following steps to configure this feature with the desired application.

## Customer Service Management configuration

To configure the mandatory skills feature for use with Customer Service Management:

-   In the Case form:
    -   Configure the form layout to use the Task Skills \[task\_m2m\_skill\] table.
    -   In the Task Skills table, set the **Mandatory** field to **True** to identify skills that are mandatory to complete a task.

        **Note:** The Case form should use either the **Skills** field or the Task Skills table, but not both.

-   \[Optional\] For existing cases that have data populated in the **Skills** field on the Case form, run the **Migrate Skills to Task Skill M2M** script to move this data to the Task Skills table. By default, this fix script migrates the skills from existing entries in the Case, Work Order, and Work Order Task tables to the Task Skills table. For more information, see [Migrate skills to the Task Skill table](../../field-service-management/task/migrate-skills-m2m-table.md).
-   If you are using the [assignment workbench](case-assignment-workbench.md), replace the **Matching Skills** matching criteria with the **Matching Skills - Mandatory Skills Support** matching criteria. For more information, see [Matching rules for case assignment](case-assignment-matching-criteria.md).

## Field Service Management configuration

To configure the mandatory skills feature for use with Field Service Management:

1.  Enable the **work.management.use.mandatory.skills** system property.
2.  Configure the Work Order form and the Work Order Task form to use the Task Skills \[task\_m2m\_skill\] table.
3.  \[Optional\] For existing work orders and tasks that have data populated in the **Skills** field on the Work Order and Work Order Task forms, run the **Migrate Skills to Task Skill M2M** script to move this data to the Task Skills table. By default, this fix script migrates the skills from existing entries in the Case, Work Order, and Work Order Task tables to the Task Skills table and configures them as optional skills. For more information, see [Migrate skills to the Task Skill table](../../field-service-management/task/migrate-skills-m2m-table.md).
4.  If you are using dynamic scheduling, update the task filter for the dynamic scheduling configuration and replace the **Matching Skills for Dynamic Scheduling** matching criteria with the **Matching Mandatory Skills for Dynamic Scheduling** matching criteria. For more information, see [Create a task filter](https://www.servicenow.com/docs/access?context=create-dynamic-scheduling-config&version=zurich&pubname=zurich-field-service-management&section=create-task-filter&ft:locale=en-US).

For configuring optional skills, navigate to **Field Service** &gt; **Administration** &gt; **Configuration**, select the **Assignment** tab and set **Auto-selection of agents for tasks requires them to have skills** to one of the following:

-   All - indicates that the agent must have all optional skills listed in the task for task assignment.
-   Some - indicates that the agent must have at least one optional skill listed in the task for task assignment.
-   None - indicates that the agent is not required to have any optional skill.

## Mandatory Skills system properties

The **Migrate Skills to Task Skill M2M** script migrates skills from existing tasks to the Task Skills \[task\_m2m\_skill\] table. Configure the task tables included in the migration using the **skills\_management.migration** system property.

The mandatory skills feature adds the following system properties.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_wwl_2yt_rdb"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

work.management.use.mandatory.skills

</td><td>

Enables the mandatory skills feature and indicates that the Task Skills \[task\_m2m\_skill\] table is being used for work orders and work order tasks. -   **Type**: true/false
-   **Default value**: false

</td></tr><tr><td>

skills\_management.migration

</td><td>

Lists the task tables to migrate to the Task Skills \[task\_m2m\_skill\] table when an admin runs the **Migrate Skills to Task Skill M2M** script. -   **Type**: choice list
-   **Default value**: wm\_task,customerservice\_case,wm\_order

</td></tr><tr><td>

com.snc.skills\_management.task\_skill\_migrated\_tables

</td><td>

Contains a list of tables for which the **Skills** field has already been migrated to the Task Skills \[task\_m2m\_skill\] table. If the table name is listed in this property, it indicates that the data is migrated and cannot be migrated again. -   **Type**: choice list
-   **Default value**: none

</td></tr></tbody>
</table>