---
title: Change the order of an answer
description: By default, the order of answer options is established when a question is created with a data type of Choice or Likert Scale.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_ChangeTheOrderOfAnAnswer.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Change the order of an answer

By default, the order of answer options is established when a question is created with a data type of **Choice** or **Likert Scale**.

## Before you begin

Role required: assessment\_admin or admin

## About this task

The system creates an Order value for each choice based on where it appears in the original list when you submit it. This order corresponds to the **Value** setting you give the answer. The choice with the lowest order number appears first, and the choice with the highest order number appears last. If you want to reconfigure the order of the answer options, you must do so by editing the **Order** field and not the **Value** field.

The **Order** column is hidden in the base system.

## Procedure

1.  Access the question record.

2.  Configure the Assessment Metric Definitions related list to display the **Order** column.

3.  Edit the order number in the list.

    **Note:** The **Value** setting remain the same for each answer option after reorganization.

    \[Omitted image "Quiz\_Answer\_Order.png"\] Alt text: Quiz answer order


**Parent Topic:**[Create an assessment metric for a category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CreateAMetric.md)

**Related topics**  


[Assessment metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentMetrics.md)

