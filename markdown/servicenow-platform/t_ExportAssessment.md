---
title: Export an assessment
description: You can share assessments between ServiceNow instances by exporting an assessment and then importing the assessment on another instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Metric types and assessable records, Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Export an assessment

You can share assessments between ServiceNow instances by exporting an assessment and then importing the assessment on another instance.

## Before you begin

Role required: assessment\_admin or admin

**Note:** Update sets are available in the Helsinki release and should be used to move data from one instance to another. For information about update sets, see System update sets.

## About this task

**Note:** The system exports a single XML file that does not contain result data.

The XML file contains a metric type `[asmt_metric_type]` and the following records that are associated with the type:

-   Assessable records `[asmt_assessable_record]`
-   Metric categories `[asmt_metric_category]`
-   Metrics `[asmt_metric]`
-   Metric definitions `[asmt_metric_definition]`
-   Category users `[asmt_m2m_category_user]`
-   Stakeholders `[asmt_m2m_stakeholder]`
-   Decision matrixes `[asmt_decision_matrix]`, `[asmt_m2m_xcategory_matrix]`, and `[asmt_m2m_ycategory_matrix]`

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Right-click the record and select **Export Assessment**.

3.  Save the XML file.


**Parent Topic:**[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

**Related topics**  


[Import an assessment](t_ImportAssessment.md)

[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

