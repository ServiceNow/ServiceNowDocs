---
title: Use automation to create standard tasks
description: Set up an automation to create a standard task that is directly related to the Industrial Guided Task \(IGT\) that triggered the standard task.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Use automation to create standard tasks

Set up an automation to create a standard task that is directly related to the Industrial Guided Task \(IGT\) that triggered the standard task.

## Before you begin

Make sure you published a standard.

Role required: sn\_icw\_igt.standard\_author

## About this task

The automation action belongs to the Action Category called Guided Task Automation, which is linked to the Assessment Template Category named Industrial Guided Task. Therefore, any assessment template created in the Industrial Guided Task category can access this automation action.

## Procedure

1.  Navigate to **Standards hub** &gt; **Standards**.

2.  Open the standard for which you want to configure the automation.

3.  Select **Advanced configuration**.

    You’re in the Smart Assessment Workspace.

4.  Provide the name and description for the new automation.

5.  Select **Create**.

6.  Select **Add standalone action set**.

7.  Select the existing **then** action set.

8.  For the field **Action type**, select **Create standard task for Automation**.

9.  On the Set actions form, fill in the fields.

    For a description of the field values, see [Standard automation task form](../reference/standard-task-automation-form.md).

10. Select **Close**.

11. Select **Activate**.

12. Select the option **I understand the automation will no longer be editable** and then select **Activate**.


**Parent Topic:**[Using Industrial Guided Tasks](../concept/using-industrial-guided-tasks.md)

