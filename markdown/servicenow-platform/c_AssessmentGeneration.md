---
title: Assessment generation
description: In the Assessments application, administrators or assessment administrators can trigger the system to generate scheduled assessments or on-demand assessments when all the prerequisite steps are completed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment generation

In the Assessments application, administrators or assessment administrators can trigger the system to generate scheduled assessments or on-demand assessments when all the prerequisite steps are completed.

An assessment administrator must publish the metric type to enable assessment generation.

The system performs these tasks when it generates assessments:

-   Creates assessment questionnaires from non-scripted metrics and assigns the questionnaires to users. When users complete their assigned questionnaires, the system uses their responses to calculate assessment results.
-   Runs scripted metrics from each category to query the database and calculate assessment results.

Each time the system generates assessments, it creates some or all of the following components. Consider having an administrator set a schedule for recurring data cleanup, as the system can potentially generate a considerable amount of assessment data.

-   [Assessment group](c_AssessmentGroups.md)
-   [Assessment instances](c_AssessmentInstances.md)
-   [Assessment results](../reference/r_AssessmentResults.md)

**Parent Topic:**[Assessment administrator tasks](c_AssessmentProcess.md)

