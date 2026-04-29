---
title: Update min and max values to match templates
description: If you use survey result calculation data, ensure that the Min and Max values for a question that uses a template are equal to the smallest and largest template definition Value.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Survey question template, Survey questions, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update min and max values to match templates

If you use survey result calculation data, ensure that the **Min** and **Max** values for a question that uses a template are equal to the smallest and largest template definition **Value**.

## Before you begin

Role required: admin or survey\_admin

## About this task

When you create a question of the **Template** data type, the system sets the **Min** and **Max** fields based on the template definition values. The fields for existing questions are not updated if you add a new template definition to a template or if you update the **Value** of an existing template. If the new **Value** is less than the minimum value or greater than the maximum value of any questions that use the template, update the questions accordingly.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Questions**.

2.  Configure the list to show the **Min** and **Max** columns.

3.  Add the following list filter condition: **\[Template\] \[is\] \[&lt;select the template you updated&gt;\]**.

4.  Ensure the **Min** and **Max** values match the smallest and largest template definition **Value** for the selected template.

    If the values do not match, edit the **Min** and **Max** values directly from the list.

    **Note:** When the data type is **Template**, a UI policy prevents the editing of **Min** and **Max** from the form.


**Parent Topic:**[Survey question template](../concept/c_SurveyQuestionTemplate.md)

**Related topics**  


[Create a survey question template](t_CreateASurveyQuestionTemplate.md)

