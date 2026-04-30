---
title: Enforce a condition to delete an assessable record
description: By default, the system does not delete assessable records, even if you change the table or conditions for the type and the existing assessable records no longer match.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assessable records, Metric types and assessable records, Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enforce a condition to delete an assessable record

By default, the system does not delete assessable records, even if you change the table or conditions for the type and the existing assessable records no longer match.

## Before you begin

Role required: assessment\_admin or admin

## About this task

The system can be configured so you can trigger the deletion of assessable records that do not match the type table and conditions.

## Procedure

1.  On the Assessment Metric Type form, select the **Enforce condition** check box to enable deletion of existing assessable records of this type that do not match the table or conditions specified.

    When the check box is cleared, the system retains existing assessable records of this type, even if they do not match the table and conditions specified.

2.  Click **Generate Assessable Records** to delete all assessable records associated with the type that do not match the current table and conditions.

    The system does not automatically delete assessable records, even if the **Enforce condition** check box is selected. You must click **Generate Assessable Records** with the check box selected every time you want the system to delete non-matching assessable records.


**Parent Topic:**[Assessable records](../concept/c_assessable-records.md)

**Related topics**  


[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

