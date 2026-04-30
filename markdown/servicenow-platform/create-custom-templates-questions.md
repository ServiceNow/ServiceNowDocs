---
title: Create custom metric type
description: Create your own custom metric type if you don’t find the metric type that you want in Survey Designer while designing surveys.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey designer, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create custom metric type

Create your own custom metric type if you don’t find the metric type that you want in Survey Designer while designing surveys.

## Before you begin

Role required: survey\_admin, survey\_creator, or admin

## About this task

You can use the Custom Metric Type module for surveys to create the custom metric type. If you set the custom metric type using the Now Mobile app, ensure that the widgets support the current theme of Mobile Employee Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Administration** &gt; **Custom Metric Type**.

2.  On the Custom Metrics page, click **New**.

3.  On the Custom Metric form, fill in the fields.

    For a description of the field values, see [Custom Metric form](../reference/custom-metric-form-fields.md).

4.  Select **Submit**.

    **Note:**

    -   Updating or deleting existing values in the **Macro**, **Widget**, and **Result type** fields might cause inconsistent effects.
    -   The custom metric type that you created doesn’t appear for the public surveys. To make it visible for the public surveys, open the Service Portal configuration and configure your survey widget to make it public. For more information about configuring widget security, see [Configure widget security](https://www.servicenow.com/docs/access?context=configure-widget-security&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
    -   If the custom metric type is inactive or deleted, the question is not rendered on the survey form.
    -   If the value in the **Macro** or **Widget** field is updated, the updated value is used to render a survey form even if an instance was created before updating the values for macros or widgets.

**Parent Topic:**[Survey designer](../concept/c_SurveyDesigner.md)

**Related topics**  


[Survey designer elements](../concept/c_SurveyDesignerElements.md)

[Configure a survey in the survey designer](t_ConfigSurveyInSurveyDesgnr.md)

[Survey categories](../concept/c_SurveyCategory.md)

[Create a question in the survey designer](t_CreateQuestSurveyDesigr.md)

[Survey question data types](../reference/r_SurveyQuestionDataTypes.md)

[Edit a survey in the survey designer](t_EditASurveyInTheSurveyDesigner.md)

[Configure category weights for a survey](t_ConfigCatWeightsForSurvey.md)

