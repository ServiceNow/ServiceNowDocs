---
title: Create a task plan template configuration
description: Admins can create configurations for task plan templates that pre-fill information in task plan template fields.Use the Plan Configuration Picker to select a pre-defined plan configuration while creating a task plan template and before authoring your template. This ensures that the correct workflow, playbook, and record page settings are applied to the template.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a task plan template configuration

Admins can create configurations for task plan templates that pre-fill information in task plan template fields.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator role

## About this task

When you create task plan template configurations, you streamline the process of creating task plan templates for your team. Configurations pre-fill fields in task plan templates, such as **Target table** and **Description**.

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Administration** &gt; **Task Plan Template Configuration**

2.  Add a brief description to the **Short description** field.

3.  Add the **Target table** you want to associate with the task plan template.

4.  Check the **Active** checkbox to active the configuration.

5.  Select **Submit**.


## Select a plan configuration when creating a task plan template

Use the Plan Configuration Picker to select a pre-defined plan configuration while creating a task plan template and before authoring your template. This ensures that the correct workflow, playbook, and record page settings are applied to the template.

### Before you begin

Role required: sn\_task\_plan.admin, sn\_task\_plan.creator role

Before creating a task plan template, confirm that at least one plan configuration has been set up on your instance.

### About this task

When you create a task plan template, the system may prompt you to select a plan configuration before the template record opens. This selection helps ensure that the template uses the correct workflow and authoring experience.

### Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** and select **New**.

    The **Plan Configuration Picker** modal opens, displaying all available plan configurations.

    **Note:** The plan configuration picker appears only when there is an active entry in the `sn_task_plan_config` table.

2.  Review the listed plan configurations and their descriptions.

3.  Select the configuration that matches your intended workflow.

    If a configuration is selected, the corresponding field is populated and the associated authoring playbook is loaded, if defined. If no configuration is selected, the task plan template is created without a configuration.

4.  Select **Create a Task Plan Template**.

5.  Complete the template fields and select **Save** to save the record.


