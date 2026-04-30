---
title: Manage an assessable record automatically
description: Define at least one filter condition in the Metric Category form to automatically associate assessable records with the category.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Assessable record associations, Assessment metric categories, View an assessment metric category, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage an assessable record automatically

Define at least one filter condition in the Metric Category form to automatically associate assessable records with the category.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Categories**.

2.  Open a category.

3.  In the **Filter** field, create a condition statement that defines the records you want to associate to this category.

    The available fields are from the table defined for the metric type. For example, for a category in the **Vendor** type, you might create the condition **\[Country\] \[is\] \[Germany\]**. Metrics in the category will be used only to evaluate vendors that are located in Germany.

4.  Save the record.

    The system associates this category to all assessable records that match the filter condition. As the system generates new assessable records that match the condition, it associates them to this category. If you change the filter condition, the system removes and creates assessable record associations, as appropriate.

    Note the following:

    -   The system does not remove assessable record associations created manually, even if the assessable records do not match the filter conditions.
    -   The system deletes any related stakeholders, if applicable, when it disassociates assessable records from a category.
    -   The system does not create or remove assessable record associations if the related source records change. For example, consider the previous example in which all assessable records for vendors based in Germany were associated to a particular category. Assume that a user changes the **Country** of one of the vendor records from **Germany** to **Canada**. The system does not disassociate the related assessable record from the category, even though it no longer matches the filter condition.
    **Note:** To configure the system to automatically associate all assessable records from a metric type to a category, use the same category condition as the metric type condition. For example, if the **Vendor** metric type has the condition **\[Vendor\] \[is\] \[true\]**, create the same condition for the category. If the metric type does not have a condition specified, you can use the category condition **\[Sys ID\] \[is not empty\]**, which includes all records from any table.


**Parent Topic:**[Assessable record associations](../reference/r_ManageAssessablRecordAssociation.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create a category for assessable records](t_CreateACategoryAR.md)

