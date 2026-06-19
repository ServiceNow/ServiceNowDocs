---
title: Migrate survey instances to Smart Assessment
description: When you migrate a survey-based questionnaire to Smart Assessment, migrate all the associated instances of a survey to Smart Assessment and re-trigger them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/mobile-experience-for-field-service-management-glide-family/migrate-survey-instances-to-smart-assessment.html
release: zurich
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrating to Smart Assessment, Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Migrate survey instances to Smart Assessment

When you migrate a survey-based questionnaire to Smart Assessment, migrate all the associated instances of a survey to Smart Assessment and re-trigger them.

## About this task

Migrate survey instances for questionnaires to Smart Assessment by manually running the job **Migrate survey instances to smart assessments**.

This job migrates all instances of a survey to Smart Assessment and re-triggers the instances.

Smart Assessment uses the Smart Assessment Engine to migrate survey instances to Smart Assessment. For more information, see .

**Note:**

-   Survey instances in **Work in progress** state can't be migrated.

-   You can link migrated instances only to Smart Assessment templates migrated from a survey-based questionnaire. Migrated instances can't be linked to a new Smart Assessment template.


## Before you begin

Role required: questionnaire\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for the **Migrate survey instances to smart assessments** job and open it.

3.  Select **Execute Now**.


## Result

Survey instances for the questionnaire are migrated to Smart Assessment and re-triggered.

