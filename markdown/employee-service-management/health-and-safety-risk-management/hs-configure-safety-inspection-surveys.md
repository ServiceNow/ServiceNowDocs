---
title: Configure a safety inspection or audit survey
description: Review surveys available with the Health and Safety Risk Management application. Modify the survey, or create one or more surveys to use for different workplaces or to check other areas of concern.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure a safety inspection or auditsurvey

Review surveys available with the Health and Safety Risk Management application. Modify the survey, or create one or more surveys to use for different workplaces or to check other areas of concern.

## Before you begin

-   Surveys are built with the ServiceNow® Survey designer. So, familiarize yourself with [Survey administration](https://www.servicenow.com/docs/access?context=r_SurveyAdminTasks&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   Ensure that the application scope is selected as Health and Safety Risk Management. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: sn\_hs\_rm.safety\_inspection\_manager, sn\_hs\_rm.safety\_audit\_manager, survey\_creator, or admin

## About this task

You can convert your existing Survey templates related to Health and Safety into Smart Assessment templates using the Smart Assessment Engine migration tool. For more information, see [Creating an assessment template from legacy assessment metric types](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Surveys** &gt; **View Surveys**.

2.  Create a new survey or modify an existing one.

    -   To create a survey, click **New** or **Survey Designer**.
    -   To modify a predefined one, filter the list to show the surveys for the Health and Safety Risk Management application and open the desired survey.
    -   For information on building and updating surveys, see [Survey designer](https://www.servicenow.com/docs/access?context=c_SurveyDesigner&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
    -   **Tip:** When assigned to a user, any survey created via the ServiceNow® Assessments and Surveys is available under **My Assessments and Surveys** in the Employee Center. Therefore, it might be a good idea that your survey has the same name as your inspection or audit record. This helps identify the inspection or audit survey quickly in the list of other assessments and surveys the user has been assigned.

3.  In the **Source table** field, select the source table.

    -   For an inspection survey, select the Inspection \[sn\_hs\_rm\_inspection\] table.
    -   For an audit survey, select the Audit survey \[sn\_hs\_rm\_audit\_survey\] table.
    **Important:** Selecting this table makes this survey available for selection in the **Inspection survey** or **Audit survey** field on respective safety inspection or audit records.


## Result

The survey is available for selection in the safety inspection or safety audit records.

## What to do next

-   Associate the survey to safety inspections or audits. You can associate any of your pre-built surveys with inspection or audit records in Health and Safety Risk Management.

-   You can also configure which survey field types should display the **Create action** check box when completing an inspection or audit from the mobile app. This enables the inspection and audit agents to create any actions on the go related to specific questions. For more information, see [Configure the create action check box for safety inspection survey in the Mobile Agent app](../../hs-health-safety-mobile/task/hs-configure-create-action-checkbox-mobile-survey.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

