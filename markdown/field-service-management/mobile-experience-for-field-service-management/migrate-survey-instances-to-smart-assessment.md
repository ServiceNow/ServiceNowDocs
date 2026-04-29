---
title: Migrate survey instances to Smart Assessment
description: When you migrate a survey-based questionnaire to Smart Assessment, migrate all the associated instances of a survey to Smart Assessment and re-trigger them.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrating to Smart Assessment, Set up Smart Assessment questionnaires, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Migrate survey instances to Smart Assessment

When you migrate a survey-based questionnaire to Smart Assessment, migrate all the associated instances of a survey to Smart Assessment and re-trigger them.

## About this task

Migrate survey instances for questionnaires to Smart Assessment by manually running the job **Migrate survey instances to smart assessments**.

This job migrates all instances of a survey to Smart Assessment and re-triggers the instances.

Smart Assessment uses the Smart Assessment Engine to migrate survey instances to Smart Assessment. For more information, see [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

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

