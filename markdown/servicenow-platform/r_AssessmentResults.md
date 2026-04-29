---
title: Assessment results
description: In the Assessments application, when the system processes completed questionnaires or gathers values returned from scripted metric queries, it generates assessment result records called metric and category results.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View a metric result, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment results

In the Assessments application, when the system processes completed questionnaires or gathers values returned from scripted metric queries, it generates assessment result records called metric and category results.

Assessment administrators can view assessment results.

The system calculates [metric results](../task/t_ViewAMetricResult.md) first, normalizes the scores, and then calculates [category results](../task/t_ViewAMetricResult.md). Each metric and category result record stores data from one assessment group, for a particular category and source record evaluated. Specifically:

-   Metric results: store data calculated from one evaluation of one metric.
-   Category results: store data calculated from a weighted average of all metrics in the category.

**Note:** Although results data is available to view in the form of metric and category result records, the most meaningful way to view results is in [scorecards](../task/t_ViewAnAssessmentScorecard.md) and decision matrixes. These tools display only the most pertinent data in graphical, comparative formats.

## Excluded Responses

The system creates metric results for responses but does not include them in category result calculations if any of the following are true:

-   The user selects the **Not Applicable** answer option on a questionnaire.
-   The user does not answer the question and the [data type](r_DataTypes.md) is not Checkbox.
-   The question data type is one of the following: Date, Date/Time, or String.
-   The metric result **Actual value**, **Scaled value**, and **Normalized value** fields are set to -1.

## Metric Attachments

After a survey or assessment is submitted, any attachments that have been added by a user are moved to the metric result record. The names of the attached files are added to the **String value** field on the Metric Result form.

**Note:** You cannot add or remove attachments from a metric result.

**Parent Topic:**[View a metric result](../task/t_ViewAMetricResult.md)

