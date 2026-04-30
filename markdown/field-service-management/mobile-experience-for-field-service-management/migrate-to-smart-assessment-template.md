---
title: Migrate a survey-based questionnaire to Smart Assessment
description: Migrate survey-based work order questionnaires and templates to Smart Assessment templates.
locale: en-US
release: yokohama
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configuring Field Service Management, Field Service Management]
---

# Migrate a survey-based questionnaire to Smart Assessment

Migrate survey-based work order questionnaires and templates to Smart Assessment templates.

## Before you begin

Role required: admin

## About this task

Administrators can migrate the existing survey-based questionnaires and templates to Smart Assessment. The migration can be started from a survey-based work order questionnaire record. A new Smart Assessment questionnaire and template is automatically created after the migration is complete.

Smart Assessment uses the Smart Assessment Engine to migrate survey-based templates to Smart Assessment templates. For more information, see [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

**Note:**

-   Smart Assessment templates don't support Boolean, Template, Percentage, Imagescale, Ranking, Rating, Duration, Custom, and Scale data types. Update these data types in work order questionnaires to the closest supported data types before initiating the migration process.
-   Conditional dependencies of a questionnaire are not migrated.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Questionnaire**.

2.  Open the questionnaire to migrate.

3.  Select **Migrate**.

4.  Select the assessment template migration record to view the status of the migration.


## Result

The questionnaire is migrated and a Smart Assessment questionnaire and template is created.

## What to do next

View, update, or publish the Smart Assessment template. For more information, see [Create or modify Smart Assessment template](create-or-modify-smart-assmt-template.md).

