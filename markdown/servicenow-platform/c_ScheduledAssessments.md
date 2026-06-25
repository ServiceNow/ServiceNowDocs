---
title: Scheduled assessments
description: The system generates a unique scheduled job for each metric type with the Schedule type field set to Scheduled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/c\_ScheduledAssessments.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Scheduled assessments

The system generates a unique scheduled job for each metric type with the **Schedule type** field set to **Scheduled**.

The system generates a unique scheduled job for each metric type with the **Schedule type** field set to **Scheduled**. Each scheduled job generates assessment components for the related metric type. By default, the scheduled job runs when an administrator executes it manually, but administrators can set a schedule to generate assessments automatically on a recurring basis.

For the system to properly generate scheduled assessments, the metric type must be active and [published](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_PublishAMetricType.md). The metric type must also be associated to at least one metric category. That metric category must be associated to one or more of each of the following items:

-   [Assessable record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_ManageAssessablRecordAssociation.md)
-   [Stakeholder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_CategoryUsersAndStakeholders.md) associated to one of the assessable records
-   [Metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentMetrics.md)

-   **[Schedule an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ScheduledAssessment.md)**  
After you have evaluated your questionnaires using on-demand assessments, edit your categories and metrics as needed, reset your metric type record, and select the users who are qualified to evaluate the assessable records.
-   **[Schedule types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ScheduleTypes.md)**  
You can schedule assessments for preconfigured users or send them to any user on demand.
-   **[Set an assessment generation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_SetAssesstGenerationSchedule.md)**  
You can set assessment generation schedules. You must set a schedule for each metric type individually.
-   **[Publish a metric type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_PublishAMetricType.md)**  
Before it is possible to generate assessments, an assessment administrator must publish the associated metric type.
-   **[Generate a scheduled assessment manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_GenSchedAssessmentManually.md)**  
Administrators can generate scheduled assessments manually.
-   **[Generate a vendor type assessment manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_GenAVendorTypeAssmtManually.md)**  
The Vendor Performance feature provides a direct method of generating assessments for the Vendor metric type.
-   **[Clean up assessment data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CleanUpAssessmentData.md)**  
The assessment process generates a considerable amount of data, some of which is not useful after a short time.
-   **[Assessment instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentInstances.md)**  
An assessment instance represents one occurrence of a questionnaire assigned to one user.
-   **[View an assessment instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ViewAnAssessmentInstance.md)**  
An assessment instance represents one occurrence of a questionnaire assigned to one user.

**Parent Topic:**[Assessment administrator tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentProcess.md)

**Related topics**  


[Assessment metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentMetrics.md)

