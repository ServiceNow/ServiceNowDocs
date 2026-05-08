---
title: Use update sets for surveys and assessments
description: Use an update set to capture changes to surveys and assessments.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Share surveys, Survey distribution, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use update sets for surveys and assessments

Use an update set to capture changes to surveys and assessments.

## Before you begin

Role required: admin or survey\_admin

## Procedure

1.  Create an update set and use it to make changes on a development instance.

    **Note:** For more information, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

    When developing surveys and assessments, use an update set to capture the changes and move them from a development instance to a production instance. Once an update set is created and marked current, all of the updates to the following tables are recorded in the update set.

    The following tables are now update set enabled and also extend the application file:

    -   Assessment Metric Templates \[asmt\_template\]
    -   Assessment metric type \[asmt\_metric\_type\]
    -   Assessment Template Definitions \[asmt\_template\_definition\]
    -   Assessment Metric Definitions \[asmt\_metric\_definition\]: survey question answer options
    -   Schedule \[sys\_trigger\]: scheduled jobs associated with the survey
    -   Assessment Metric Categories \[asmt\_metric\_category\]: survey categories
    -   Assessment Metrics \[asmt\_metric\]: survey questions
    -   Assessment Category Users \[asmt\_m2m\_category\_user\]: survey users
    -   Trigger Conditions \[asmt\_condition\]

**Parent Topic:**[Sharing surveys](../concept/c_SurveyInportAndExport.md)

**Parent Topic:**[Metric types and assessable records](../../assessments/concept/c_MetricTypesAndAssessableRecords.md)

