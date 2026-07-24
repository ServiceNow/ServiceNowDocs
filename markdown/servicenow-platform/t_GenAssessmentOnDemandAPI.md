---
title: Generate an assessment with the on-demand API
description: The Assign Assessment buttons call an API to generate on-demand assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_GenAssessmentOnDemandAPI.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [On-demand assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate an assessment with the on-demand API

The Assign Assessment buttons call an API to generate on-demand assessments.

## Before you begin

Role required: assessment\_admin or admin

## About this task

## Procedure

1.  To generate an assessment, call the [AssessmentCreation API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_AssessmentCreation.md) from any script in the system, such as a business rule or client script.

2.  Use the sys\_ids of these items:

    -   An assessable record to evaluate. The assessable record must be associated with an on-demand type and at least one category that contains non-scripted metrics.
    -   One or more users who should perform the assessment. The API generates a questionnaire about the specified assessable record for each user.

**Parent Topic:**[On-demand assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_OnDemandAssessments.md)

**Related topics**  


[Assessment generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentGeneration.md)

[Scheduled assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ScheduledAssessments.md)

[Generate a scheduled assessment manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_GenSchedAssessmentManually.md)

[Generate a vendor type assessment manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_GenAVendorTypeAssmtManually.md)

[Set an assessment generation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_SetAssesstGenerationSchedule.md)

[Assessment instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_AssessmentInstances.md)

[View an assessment instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ViewAnAssessmentInstance.md)

[Clean up assessment data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CleanUpAssessmentData.md)

