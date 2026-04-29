---
title: Create an employee form
description: Create or modify an employee form to collect employee input. Employee forms are questionnaires that are built using the survey designer to collect or update information from employees.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Universal Task, Universal Task, Employee Service Management]
---

# Create an employee form

Create or modify an employee form to collect employee input. Employee forms are questionnaires that are built using the survey designer to collect or update information from employees.

## Before you begin

To use this task, first create an employee form record. Then, use the survey designer to design a questionnaire for the employee.

Role required: sn\_uni\_task.emp\_form\_admin or sn\_uni\_task.emp\_form\_creator

**Note:** You will need sn\_hr\_le.activity\_reader role or any role that starts with sn\_hr\_core to have read access to the employee form page being utilized, and view data that is passed between case and child task.

## Procedure

1.  Navigate to **All** &gt; **Universal tasks** &gt; **Employee forms**.

2.  Click **Create New**.

3.  On the form, fill in the fields.

    For more information on form fields and descriptions, see [Employee form](../reference/ut-emp-form.md).

4.  Right-click the form header and click **Save**.

    The **Form designer** button appears.

5.  To open the survey designer in a new window, click **Form designer**.

6.  To build the questions for your employee form, use the survey designer.

    For more information on the question types, see [Survey designer elements](https://www.servicenow.com/docs/access?context=c_SurveyDesignerElements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

7.  Click **Save and Publish**.


## Result

You can now assign the form to an employee by using the Collect Employee input task. To view the employee responses, click **View Responses** after the task is marked complete.

**Note:** You must have specific roles to view the employee responses. For more information, see [Configure the roles to view employee forms](ut-config-empform-view-roles.md)

**Parent Topic:**[Using Universal Task](../concept/use-universal-task.md)

