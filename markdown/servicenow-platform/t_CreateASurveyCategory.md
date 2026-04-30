---
title: Create a survey category in a survey
description: You can modify an existing survey to add one or more survey categories.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Survey categories, Survey designer, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a survey category in a survey

You can modify an existing survey to add one or more survey categories.

## Before you begin

Role required: admin or survey\_admin

## About this task

Only one category is required for each survey, but you can add additional categories as needed.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition.

3.  In the **Metric Categories** related list, open a category or click **New**.

    Each survey category is stored as a record on the Metric Category \[asmt\_metric\_category\] table with a modified view for survey use.

4.  Enter the survey category name and description.

    The category name appears on questionnaires when either of the following is true.

    -   There is more than one category for the survey.
    -   There is only one category and its name is different from the survey definition name. If you create a survey using the survey creator, the category name is the same as the survey definition name.
5.  Right-click the form header and click **Save**.

    The **Assessment Metrics** and **Users** related lists appear.

6.  Click **Update**.


**Parent Topic:**[Survey categories](../concept/c_SurveyCategory.md)

**Related topics**  


[Create a category in the survey designer](t_CreateCatInSurveyDesigr.md)

