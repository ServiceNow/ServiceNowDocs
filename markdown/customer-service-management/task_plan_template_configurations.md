---
title: Create a task plan template configuration
description: Admins can create configurations for task plan templates that pre-fill information in task plan template fields.Use the Plan Configuration Picker to select a pre-defined plan configuration while creating a task plan template and before authoring your template. This ensures that the correct workflow, playbook, and record page settings are applied to the template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/task\_plan\_template\_configurations.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 3
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a task plan template configuration

Admins can create configurations for task plan templates that pre-fill information in task plan template fields.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator

## About this task

When you create task plan template configurations, you streamline the process of creating task plan templates for your team. Configurations pre-fill fields in task plan templates, such as **Target table** and **Description**.

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Administration** &gt; **Task Plan Template Configuration**

2.  Add a brief description to the **Short description** field.

3.  Add the **Target table** you want to associate with the task plan template.

4.  Select an icon to associate with this configuration.

    The icon helps you visually distinguish this configuration from others when selecting a configuration in the **Plan Configuration Picker**.

5.  Check the **Active** checkbox to active the configuration.

6.  Select **Submit**.

7.  Create template item configurations as children of this task plan template configuration.

    You create them from the Template Item Configuration table \(`sn_task_plan_template_item_config`\). All fields in this table function the same way as the corresponding fields in the Template Item table. For field descriptions, see [Template item form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-template-item-form.md).

    To select a template item configuration when you create a template item, the parent task plan template must have its **Template Configuration** field populated, and that task plan template configuration must have associated template item configuration records.

    **Note:** When you create a template item, if you select a template item configuration, the **Tracking fields** section is hidden. Those fields are then automatically populated from the selected template item configuration record.

8.  To apply configuration changes to draft templates or template items already created from it, open the configuration record, make the changes, and select **Save and cascade**.

    **Save** applies changes only to templates or template items created going forward. Existing ones are not updated.

    **Save and cascade** applies changes to all draft templates and template items linked to the configuration. Published templates and items are not affected.

    **Note:** Save and cascade only applies changes made on the configuration form itself — you can't edit a linked template item directly from the configuration's related list. To change a value on an individual template item, open that item's own form.


## Select a plan configuration when creating a task plan template

Use the Plan Configuration Picker to select a pre-defined plan configuration while creating a task plan template and before authoring your template. This ensures that the correct workflow, playbook, and record page settings are applied to the template.

### Before you begin

Role required: sn\_task\_plan.admin, sn\_task\_plan.creator role

Before creating a task plan template, confirm that at least one plan configuration has been set up on your instance.

### About this task

When you create a task plan template, the system may prompt you to select a plan configuration before the template record opens. This selection helps ensure that the template uses the correct workflow and authoring experience.

If an icon has been set on a configuration, that icon is displayed alongside the configuration in the picker to help you tell configurations apart.

### Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** and select **New**.

    The **Plan Configuration Picker** modal opens, displaying all available plan configurations.

    **Note:** The plan configuration picker appears only when there is an active entry in the `sn_task_plan_config` table.

2.  Review the listed plan configurations and their descriptions.

3.  Select the configuration that matches your intended workflow.

    If a configuration is selected, the corresponding field is populated and the associated authoring playbook is loaded, if defined. If no configuration is selected, the task plan template is created without a configuration.

4.  Select **Create a Task Plan Template**.

5.  Complete the template fields and select **Save** to save the record.


