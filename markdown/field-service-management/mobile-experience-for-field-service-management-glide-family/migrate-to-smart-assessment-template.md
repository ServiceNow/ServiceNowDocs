---
title: Migrate a survey-based questionnaire to Smart Assessment
description: Migrate survey-based work order questionnaires and templates to Smart Assessment templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/mobile-experience-for-field-service-management-glide-family/migrate-to-smart-assessment-template.html
release: zurich
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrating to Smart Assessment, Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Migrate a survey-based questionnaire to Smart Assessment

Migrate survey-based work order questionnaires and templates to Smart Assessment templates.

## Before you begin

Role required: admin

## About this task

Administrators can migrate the existing survey-based questionnaires and templates to Smart Assessment. The migration can be started from a survey-based work order questionnaire record. A new smart assessment questionnaire and template is automatically created after the migration is complete.

Smart Assessment uses the Smart Assessment Engine to migrate survey-based templates to Smart Assessment templates. For more information, see [Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/smart-assessment-engine/smart-asmnt-engine-landing-page.md).

**Note:**

-   Smart Assessment templates don't support Boolean, Template, Percentage, Imagescale, Ranking, Rating, Duration, Custom, and Scale data types. Update these data types in work order questionnaires to the closest supported data types before initiating the migration process.
-   Conditional dependencies of a questionnaire are not migrated.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Questionnaire**.

2.  Open the questionnaire to migrate.

3.  Select **Migrate**.

    Migration initiation confirmation displays.

4.  Select the assessment template migration record to view the status of the migration.


## Result

The questionnaire is migrated and a Smart Assessment questionnaire and template is created.

## What to do next

To view, update, or publish the Smart Assessment template, navigate to **Workspaces** &gt; **Assessment Workspace**. For more information, see [Author and publish a Smart Assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/mobile-experience-for-field-service-management-glide-family/create-a-smart-assessment-template.md).

