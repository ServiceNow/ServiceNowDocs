---
title: View the results for a survey
description: You can view the responses for one survey definition. Survey results are stored on the Metric Result \[asmt\_metric\_result\] table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Survey responses and results, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View the results for a survey

You can view the responses for one survey definition. Survey results are stored on the Metric Result \[asmt\_metric\_result\] table.

## Before you begin

Role required: survey\_admin or survey\_reader

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition.

3.  Under **Related Links**, select **View Responses** to view information regarding each user's response.

    The results are grouped by metric, which is what questions are called in assessments.

4.  Under **Related Links**, select **View Scorecard** review the compiled data of all responses represented in pie charts.

    For detailed information, see [View a survey scorecard](t_ViewAScorecard.md).

5.  Open a metric result to view more detail.

    The metric result contains the user's response and calculated values of interest to advanced survey administrators. Because the Metric Result table is also used by the assessment feature, many field names aren’t clear in the context of surveys.

    ![Metric result](../image/AssessmentMetricResults.png)

    For a description of the field values, see [Metric Result form](../reference/r_MetricResultFieldNames.md).


**Parent Topic:**[Survey responses and results](../concept/c_SurveyResults.md)

**Related topics**  


[View results for all surveys](t_ViewResultsForAllSurveys.md)

[View a survey scorecard](t_ViewAScorecard.md)

[Export a quiz scorecard as an image](../../assessments/task/t_ExportAQuizScorecard.md)

[Request translations for surveys](request-translations-for-surveys.md)

[Edit translations for surveys](edit-translations-for-surveys.md)

[Survey responses in a database view](../concept/survey-result-database-view.md)

