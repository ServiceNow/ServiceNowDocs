---
title: Update a metric minimum and maximum value to match a template
description: For assessment results to be properly calculated, the Min and Max values of a metric that uses a template must be equal to the smallest and largest template definition Value, respectively.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a metric template, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update a metric minimum and maximum value to match a template

For assessment results to be properly calculated, the Min and Max values of a metric that uses a template must be equal to the smallest and largest template definition Value, respectively.

## Before you begin

Role required: assessment\_admin or admin

## About this task

The system sets the **Min** and **Max** fields automatically when you create a metric of the Template data type, based on the template definition values. However, the system does not update these fields for existing metrics if you add a new template definition to a template or if you update the Value of an existing template definition. If the new Value is less than the minimum value of any metrics that use the template or greater than the maximum value, update the metrics accordingly.

To edit the minimum and maximum values for a question that has the Template data type:

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Metrics**.

2.  Configure the [Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/t_ConfigureTheListLayout.md) to show the **Min** and **Max** columns.

3.  Run the following list filter condition: `[Template] [is] [<select the template you updated>]`

4.  Ensure the Min and Max values match the smallest and largest template definition Value for the selected template, respectively.

    If the values do not match, edit the Min and Max directly from the list.

    **Note:** When the data type is Template, a UI policy prevents the editing of Min and Max from the form.


**Parent Topic:**[Create a metric template](t_CreateAMetricTemplate.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create an assessment metric for a category](t_CreateAMetric.md)

[Create an assessment metric definition](t_CreateAMetricDefinition.md)

