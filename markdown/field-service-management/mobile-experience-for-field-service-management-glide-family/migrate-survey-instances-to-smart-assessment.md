---
title: Migrate survey instances to Smart Assessment
description: Migrate a survey-based questionnaire to Smart Assessment, which migrates all the associated instances of a survey to Smart Assessment and re-triggers them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/mobile-experience-for-field-service-management-glide-family/migrate-survey-instances-to-smart-assessment.html
release: yokohama
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configuring Field Service Management, Field Service Management]
---

# Migrate survey instances to Smart Assessment

Migrate a survey-based questionnaire to Smart Assessment, which migrates all the associated instances of a survey to Smart Assessment and re-triggers them.

## About this task

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

