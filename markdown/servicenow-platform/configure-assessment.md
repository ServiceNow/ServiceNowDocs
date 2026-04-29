---
title: Configure an assessment
description: You can create a new assessment on a selected assessable records to evaluate, score, and rank records from any table in the system. Then create a metric category and assessment metrics for the assessment, publish the assessment, and assign it to the selected users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure an assessment

You can create a new assessment on a selected assessable records to evaluate, score, and rank records from any table in the system. Then create a metric category and assessment metrics for the assessment, publish the assessment, and assign it to the selected users.

## Before you begin

Role required: admin, survey\_creator, or assessment\_admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Click **New**.

3.  On the Assessment Metric form, fill in the fields.

    For a description of the field values, see [Assessment Metric form](../reference/assessment-metric-form.md).

4.  Create a new assessment and assign it to the assessors.

    Do the following in the Assessment Metric form.

    1.  Add a condition: In the **Condition** tab, add a condition to define the assessable records on which the assessment is created.
    2.  Add decision matrix fields: In the **Decision Matrix** tab, add the required filter field to identify filter menu choices on decision matrices and scorecard averages for this type. For more information, see [Decision matrixes](../reference/r_AdministerDecisionMatrixes.md) .
    3.  Select the Assessors: In the **Assessors** tab, select the users to whom the assessment will be assigned.
    4.  Generate Assessable records: When you save the assessment and click **Generate Assessable Records**, an assessable record is created for each unique user of the user field.

        **Note:**

        -   You must generate the assessable records, each time you update the condition.
        -   You can generate the assessable records only after updating the condition.
        A new assessment is created. You must now create metric category and add assessment metrics to each metric category. Then publish the assessment and assign the assessment to the selected users.

    5.  Create a metric category: To create a metric category, do the following:
        1.  Open the assessment you just created and click **New** in the **Metric Categories** tab. Fill the form.

            For more information about form fields, see [Metric Category form](../reference/metric-category-form.md)form.

            **Tip:** To know how to create metric category alternatively, see [Create a category for assessable records](t_CreateACategoryAR.md).

        2.  Open a metric category, add a condition, and click **Assessable records** tab. The assessable records appear based on the selection made in the metric category form.
        3.  Open a metric category, click **Assessment Metric** tab to add the questions. Click **New**.

            For more information about form fields, see [Assessment Metric form for a category](../reference/assessment-metric-category-form.md).

            **Tip:** To know how to create assessment metric category alternatively, see [Create an assessment metric for a category](t_CreateAMetric.md).

    6.  Click **Publish**, to publish the assessment. For more information, see [Publish a metric type](t_PublishAMetricType.md).
    7.  Assign the Assessment to the required users. Do the following:
        1.  For an on-demand Assessments, click either the **Assign Assessment** or **Assign to Assessors** link to assign the assessment. For more information, see [Generate an on-demand assessment for multiple assessable records](t_GenOnDemandAssessMultAssessRec.md).
        2.  For a scheduled Assessment, click the **Generate Assessments ** link to trigger the scheduled job immediately. For more information, see [Generate a scheduled assessment manually](t_GenSchedAssessmentManually.md).

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)

