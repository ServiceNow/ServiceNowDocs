---
title: Scheduled assessments
description: The system generates a unique scheduled job for each metric type with the Schedule type field set to Scheduled.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Scheduled assessments

The system generates a unique scheduled job for each metric type with the **Schedule type** field set to **Scheduled**.

The system generates a unique scheduled job for each metric type with the **Schedule type** field set to **Scheduled**. Each scheduled job generates assessment components for the related metric type. By default, the scheduled job runs when an administrator executes it manually, but administrators can set a schedule to generate assessments automatically on a recurring basis.

For the system to properly generate scheduled assessments, the metric type must be active and [published](../task/t_PublishAMetricType.md). The metric type must also be associated to at least one metric category. That metric category must be associated to one or more of each of the following items:

-   [Assessable record](../reference/r_ManageAssessablRecordAssociation.md)
-   [Stakeholder](../reference/r_CategoryUsersAndStakeholders.md) associated to one of the assessable records
-   [Metric](c_AssessmentMetrics.md)

-   **[Schedule an assessment](../task/t_ScheduledAssessment.md)**  
After you have evaluated your questionnaires using on-demand assessments, edit your categories and metrics as needed, reset your metric type record, and select the users who are qualified to evaluate the assessable records.
-   **[Schedule types](c_ScheduleTypes.md)**  
You can schedule assessments for preconfigured users or send them to any user on demand.
-   **[Set an assessment generation schedule](../task/t_SetAssesstGenerationSchedule.md)**  
You can set assessment generation schedules. You must set a schedule for each metric type individually.
-   **[Publish a metric type](../task/t_PublishAMetricType.md)**  
Before it is possible to generate assessments, an assessment administrator must publish the associated metric type.
-   **[Generate a scheduled assessment manually](../task/t_GenSchedAssessmentManually.md)**  
Administrators can generate scheduled assessments manually.
-   **[Generate a vendor type assessment manually](../task/t_GenAVendorTypeAssmtManually.md)**  
The Vendor Performance feature provides a direct method of generating assessments for the Vendor metric type.
-   **[Clean up assessment data](../task/t_CleanUpAssessmentData.md)**  
The assessment process generates a considerable amount of data, some of which is not useful after a short time.
-   **[Assessment instances](c_AssessmentInstances.md)**  
An assessment instance represents one occurrence of a questionnaire assigned to one user.
-   **[View an assessment instance](../task/t_ViewAnAssessmentInstance.md)**  
An assessment instance represents one occurrence of a questionnaire assigned to one user.

**Parent Topic:**[Assessment administrator tasks](c_AssessmentProcess.md)

**Related topics**  


[Assessment metrics](c_AssessmentMetrics.md)

