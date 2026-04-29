---
title: Legacy survey migration
description: Users with the survey\_admin role can migrate legacy survey data to create copies of legacy surveys and their related records in assessment tables. The Survey Management application, which is built on the assessment engine, is available as an alternative to legacy surveys.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Legacy survey migration

Users with the survey\_admin role can migrate legacy survey data to create copies of legacy surveys and their related records in assessment tables. The Survey Management application, which is built on the assessment engine, is available as an alternative to legacy surveys.

The following legacy survey components are migrated:

-   Survey masters
-   Supported survey questions and question choices
-   Survey instances
-   Survey responses

Legacy survey conditions are not migrated and must be recreated as trigger conditions.

**Note:**

-   The **Legacy Surveys** and **Legacy Administration** modules are available on instances upgraded from a previous release but not available for new instances. Customers using legacy survey or survey wizard should plan to migrate to the Survey Management application to create modern and high quality surveys for their users.
-   The following legacy survey plugins are inactive by default, and are available upon request:
    -   Best Practice - Task Survey Management \(ID: com.snc.bestpractice.task\_survey\)
    -   Survey Management \(ID: com.glideapp.survey\)
    -   Assessment Components \(ID: com.snc.assessment\)
    -   Survey Wizard \(ID: com.glideapp.survey\_wizard\)
-   Survey wizards cannot be migrated.

-   **[Migrate a legacy survey](../task/t_MigrateALegacySurvey.md)**  
Migrate a legacy survey and its related records to take advantage of a more powerful feature set.
-   **[Survey question migration](../reference/r_SurveyQuestionMigration.md)**  
Before you migrate a legacy survey, understand that some legacy survey questions cannot be migrated due to incompatible question types.
-   **[Migrated components](../reference/r_MigratedComponents.md)**  
When you migrate a survey, the system maps records from survey tables to assessment tables.
-   **[Migrated question review](../reference/r_ReviewMigratedQuestions.md)**  
To maintain accurate result calculations, you may need to make minor adjustments to some of the migrated survey records to ensure results are calculated correctly.

**Parent Topic:**[Survey administration](../reference/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports](../task/view-survey-overview.md)

[Survey designer](c_SurveyDesigner.md)

[View a survey instance](../task/t_ViewSurveyInstance.md)

[Survey users and groups](c_SurveyUsersAndGroups.md)

[Copy a survey](../task/copy-survey.md)

[Publish a survey](../task/t_PublishASurvey.md)

[Customize the appearance of a survey](../task/t_CustomizingAppearance.md)

[Survey definitions](c_SurveyDefinitions.md)

[Create a survey designer template question](../task/t_CreateASurveyDesignerTemplateQ.md)

[Survey questions](c_SurveyQuestion.md)

[Survey trigger conditions](c_TriggerConditions.md)

[Survey distribution](c_SurveyDistribution.md)

[Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md)

[Sentiment analysis for surveys](sentiment-analysis.md)

[Surveys in Service Portal and the Now Mobile app](c_SurveyServicePortal.md)

[Surveys in ITSM Virtual Agent](survey-virtual-agent.md)

