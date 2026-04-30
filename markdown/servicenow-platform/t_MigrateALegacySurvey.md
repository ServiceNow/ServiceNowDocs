---
title: Migrate a legacy survey
description: Migrate a legacy survey and its related records to take advantage of a more powerful feature set.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy survey migration, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrate a legacy survey

Migrate a legacy survey and its related records to take advantage of a more powerful feature set.

## Before you begin

Role required: admin or survey\_admin

## About this task

To avoid timing out for very large surveys, you can disable the transaction quota. See [Transaction quotas](https://www.servicenow.com/docs/access?context=c_TransactionQuotas&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Legacy Surveys** &gt; **Masters**.

    The list of legacy survey masters appears. By default, the list shows only survey masters that have not been migrated. To show all survey masters, remove the **Assessment is empty** breadcrumb.

2.  Open a survey and click the **Migrate to New Survey Management** related link or **Migrate to New Survey Management** in the title bar.

    A dialog box describes what happens when you migrate the survey. Note that certain types of survey questions cannot be migrated.

3.  Click **OK**.

    The system generates records on assessment tables based on the survey master, eligible questions and choices, results, and other related survey components. The original survey components are unaffected.

    System messages may appear at the top of the Survey form to notify you of questions that could not be migrated and to advise you to review migrated **Multiple Choice** questions.

4.  Click the reference icon beside the **Assessment** field to view the new survey definition.

5.  Remove survey users from the assessment survey if you want all users to be able to take it.

    When you migrate a survey, any users who have taken it are automatically associated with the assessment survey and become survey users. When there are survey users associated with an assessment survey, only those users can take it.

6.  Deactivate any survey conditions associated with the survey by completing the following steps.

    1.  Navigate to **Survey** &gt; **Legacy Administration** &gt; **Survey Conditions**.

    2.  In the **Active** column, ensure the value is false for any survey conditions that reference the migrated survey.

7.  Navigate to **Survey** &gt; **Administration** &gt; **Trigger Conditions** to create new trigger conditions for the migrated survey.


## Result

The **Migrate to Assessment** related link on the legacy survey record becomes unavailable after the migration. However, if you delete the record referenced in the **Assessment** field, the related link reappears and you can migrate the legacy survey again.

**Parent Topic:**[Legacy survey migration](../concept/c_MigrateSurveys.md)

**Related topics**  


[Survey question migration](../reference/r_SurveyQuestionMigration.md)

[Migrated components](../reference/r_MigratedComponents.md)

[Migrated question review](../reference/r_ReviewMigratedQuestions.md)

