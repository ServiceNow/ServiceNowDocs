---
title: Create a survey question template
description: You can create and administer question templates.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Survey question template, Survey questions, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a survey question template

You can create and administer question templates.

## Before you begin

Role required: admin or survey\_admin

## About this task

Changes to a survey, such as the modification of question templates, apply to existing survey instances immediately. Templates that you create are available for use with both surveys and assessments.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Templates**.

    Each template is stored as a record on the Assessment Metric Template \[asmt\_template\] table.

2.  Click **New**.

3.  Enter a **Name**.

4.  Right-click the form header and click **Save**.

5.  In the **Assessment Template Definitions** related list, click **New**.

    Create a template definition for each answer option you want to appear on a question.

6.  Complete the form.

<table id="table_kvd_34r_n5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display

</td><td>

Enter the text to appear as the answer option.

</td></tr><tr><td>

Value

</td><td>

Enter a numeric value, greater than or equal to zero, to which the answer option equates. Values are used in results calculations. When you view questions that use templates, answer options appear in order from smallest to largest **Value**. Each template definition for a given template must have a unique **Value**.

</td></tr></tbody>
</table>7.  Click **Update**.


**Parent Topic:**[Survey question template](../concept/c_SurveyQuestionTemplate.md)

**Related topics**  


[Update min and max values to match templates](t_UpdateQMinAndMaxToMatchTemplates.md)

