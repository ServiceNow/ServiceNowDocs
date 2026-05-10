---
title: Generate an assessment with the on-demand API
description: The Assign Assessment buttons call an API to generate on-demand assessments.
locale: en-US
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

**Parent Topic:**[On-demand assessments](../concept/c_OnDemandAssessments.md)

**Related topics**  


[Assessment generation](../concept/c_AssessmentGeneration.md)

[Scheduled assessments](../concept/c_ScheduledAssessments.md)

[Generate a scheduled assessment manually](t_GenSchedAssessmentManually.md)

[Generate a vendor type assessment manually](t_GenAVendorTypeAssmtManually.md)

[Set an assessment generation schedule](t_SetAssesstGenerationSchedule.md)

[Assessment instances](../concept/c_AssessmentInstances.md)

[View an assessment instance](t_ViewAnAssessmentInstance.md)

[Clean up assessment data](t_CleanUpAssessmentData.md)

