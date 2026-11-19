---
title: Edit a survey in the survey designer
description: You can modify surveys using the survey designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/t\_EditASurveyInTheSurveyDesigner.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Survey designer, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a survey in the survey designer

You can modify surveys using the survey designer.

## Before you begin

Role required: admin or survey\_admin

## About this task

You can edit a survey even after it has been distributed, with the following results.

-   Added questions are available only on surveys that are distributed after this change.
-   Changes to existing questions are immediately available to users before the survey is submitted or during the retake period. This includes changes to the answers, such as additional choices or changes to the data type.
-   Deleted questions are also deleted from the distributed surveys in user queues.

**Note:** You can only edit a survey that has the same application scope as that of your current session.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Survey Designer**.

2.  Point to the menu icon in the survey header bar, and select **Load Survey**.

3.  Select a survey from the list and modify it as needed.

4.  Point to the menu icon in the survey header bar, and select **Save** or **Save and Publish**.

    When you publish the edited survey, the system generates survey instances for any associated survey users.


**Parent Topic:**[Survey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/c_SurveyDesigner.md)

**Related topics**  


[Survey designer elements]()

[Configure a survey in the survey designer]()

[Survey categories]()

[Create a question in the survey designer]()

[Survey question data types]()

[Create custom metric type]()

[Configure category weights for a survey]()

