---
title: Assessment generation
description: In the Assessments application, administrators or assessment administrators can trigger the system to generate scheduled assessments or on-demand assessments when all the prerequisite steps are completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/ai-platform-capabilities/c\_AssessmentGeneration.html
release: zurich
product: AI Platform Capabilities
classification: ai-platform-capabilities
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment generation

In the Assessments application, administrators or assessment administrators can trigger the system to generate scheduled assessments or on-demand assessments when all the prerequisite steps are completed.

An assessment administrator must publish the metric type to enable assessment generation.

The system performs these tasks when it generates assessments:

-   Creates assessment questionnaires from non-scripted metrics and assigns the questionnaires to users. When users complete their assigned questionnaires, the system uses their responses to calculate assessment results.
-   Runs scripted metrics from each category to query the database and calculate assessment results.

Each time the system generates assessments, it creates some or all of the following components. Consider having an administrator set a schedule for recurring data cleanup, as the system can potentially generate a considerable amount of assessment data.

-   [Assessment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/ai-platform-capabilities/c_AssessmentGroups.md)
-   [Assessment instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/ai-platform-capabilities/c_AssessmentInstances.md)
-   [Assessment results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/ai-platform-capabilities/r_AssessmentResults.md)

**Parent Topic:**[Assessment administrator tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/ai-platform-capabilities/c_AssessmentProcess.md)

