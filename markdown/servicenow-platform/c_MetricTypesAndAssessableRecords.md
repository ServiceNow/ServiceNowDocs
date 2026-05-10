---
title: Metric types and assessable records
description: In the Assessments application, assessment administrators create and administer metric types and assessable records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Metric types and assessable records

In the Assessments application, assessment administrators create and administer metric types and assessable records.

A metric type defines a set of records an organization wants to evaluate, such as vendors, projects, or employees. For each type, the system generates unique assessable records that link the type to records that need to be evaluated, such as the individual records for the vendors Amazon and Intel. There may be multiple assessable records for the same source record if the source record meets the criteria for more than one type. For example, you might want to evaluate a record on the Company table, such as Intel, as a vendor and as a manufacturer, with different [categories](../reference/r_CategoryMetrics.md) and [metrics](c_AssessmentMetrics.md).

For configuration suggestions, see [Assessment administrator tasks](c_AssessmentProcess.md).

## Assessable records

An assessable record links a source record you want to evaluate, such as the company record for Amazon or the user record for a sales representative, to a metric type, such as vendors or employees.

You use assessments to evaluate the assessable record. The system generates assessable records from the source records that match the table and conditions set on the Assessment Metric Type form. You evaluate the assessable records with metric categories and metrics, which define traits and values to assess. For metric types with the **On demand** schedule type, you can [generate on-demand assessments](../task/t_GenOnDemandAssessOneAssessRec.md) from the Assessable Record form. This method of assessment generation makes it easy to create and preview short questionnaires or to quickly obtain assessment results for specific assessable records.

You can set up an assessment description that includes information from multiple fields on an assessable record and is displayed on multiple lines. This set up provides the user who is taking the assessment with a more detailed and understandable description of the information being requested on the assessment questionnaire. Create a multi-line description using table titles, which can be defined to use one or more fields from the selected table.

-   **[Create metric types and generate assessable records](../task/t_CreatMetricTypesAndGenAssessRecs.md)**  
Create a metric type, which sets a table and filter conditions that define a set of records to evaluate.
-   **[Delete a metric type](../task/t_DeleteAMetricType.md)**  
Deleting a metric type entails deleting many related records.
-   **[Export an assessment](../task/t_ExportAssessment.md)**  
You can share assessments between ServiceNow instances by exporting an assessment and then importing the assessment on another instance.
-   **[Import an assessment](../task/t_ImportAssessment.md)**  
Share assessments between ServiceNow instances by importing a previously exported assessment.
-   **[Use update sets for surveys and assessments](../../survey-administration/task/t_UseUpdateSetsForSurveyAssess.md)**  
Use an update set to capture changes to surveys and assessments.
-   **[Create an assessment signature](../task/t_CreateAnAssessmentSignature.md)**  
A signature on an assessment questionnaire contains assertions that can communicate directions, a legal statement, or any text that you want the recipient to consider.
-   **[Assessable records](c_assessable-records.md)**  
An assessable record links a source record you want to evaluate, such as the company record for Amazon or the user record for a sales representative, to a metric type, such as vendors or employees.
-   **[Delete an assessable record](../task/t_DeleteAssessableRecord.md)**  
When you delete an assessable record, the system deletes any stakeholders for the record.
-   **[View an assessable record](../task/t_ViewAnAssessableRecord.md)**  
View the Assessable Record form to edit preferences and perform various actions.

**Parent Topic:**[Create an assessment metric for a category](../task/t_CreateAMetric.md)

**Parent Topic:**[Using assessments](using-assessments.md)

**Related topics**  


[Use update sets for surveys and assessments](../../survey-administration/task/t_UseUpdateSetsForSurveyAssess.md)

[Metric types and assessable records](c_MetricTypesAndAssessableRecords.md)

[View an assessable record](../task/t_ViewAnAssessableRecord.md)

