---
title: Modify a survey definition
description: You can configure additional options for a survey definition.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Survey definitions, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modify a survey definition

You can configure additional options for a survey definition.

## Before you begin

Role required: admin, survey\_creator, or survey\_admin

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

    Each survey definition is stored as a record on the Assessment Metric Type `[asmt_metric_type]` table with a modified view for survey use.

2.  Open a survey definition.

    The **Response Trend** chart with the weekly trend of the survey instance count, and the **Survey Summary** chart with the overall summary response based on instance states are displayed.

3.  Modify the fields on the Survey Definition form.

    **Note:** You can only edit a survey that has the same application scope as that of your current session.

<table id="table_j23_ml4_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="tr_SurveyName"><td>

Name

</td><td>

Name of the survey which appears on the questionnaire.

</td></tr><tr id="tr_SurveyDescription"><td>

Description

</td><td>

Helpful information about the survey.

</td></tr><tr id="tr_SurveyActive"><td>

Active

</td><td>

Check box to activate the survey definition. When the **Active** check box is cleared, new survey instances cannot be generated and users cannot complete existing survey instances. Use the **Active** check box to deactivate or activate a published survey.

</td></tr><tr><td>

Owners

</td><td>

Owners of the survey. You can add a user with the survey\_creator, survey\_admin, or assessment\_admin role.

</td></tr><tr id="tr_SurveyAnonymous"><td>

Anonymize responses

</td><td>

Check box to ensure that all responses for this survey are stored without the submitting user names. When a user submits a survey, the system clears the **Assigned to** field for the associated survey instance. Also, survey responses for anonymous surveys do not contain **Assigned to** values.**Note:** The **Assigned to** field is cleared. However, each response record includes the **Created By** and **Updated By** fields that are accessible to users with the survey\_admin role.

</td></tr><tr id="tr_SurveyState"><td>

State

</td><td>

Status of the survey: **Draft** or **Published**.

</td></tr><tr><td>

Allow retake

</td><td>

Check box that allows users to modify their answers to a completed survey. Users can resubmit a survey as many times as they want until the due date. After that date, the system removes the survey from the user's My Assessments &amp; Surveys page.

</td></tr><tr><td>

Scheduled job

</td><td>

Scheduled job that the system creates for this survey definition when the schedule period is a repeating interval. The system sets the scheduled job to run according to the selected schedule period.-   If you change the schedule period and save the survey definition, the system deletes the old scheduled job.
-   If you selected a recurring schedule period, a new scheduled job is created.
For example, if you change the schedule period from **Daily** to **Weekly** and save the record:-   The system deletes the daily scheduled job.
-   Creates a weekly one set to run a week from the current date.
 This field is visible to administrators only if the schedule period is **Daily**, **Weekly**, **Monthly**, or **Yearly**.

</td></tr><tr><td>

Assessment duration

</td><td>

The length of time to complete assigned survey instances, starting from the time the survey instance is generated. The assessment duration sets the Due date for each survey instance. The default duration is 14 days. Configure the form to view this field.

</td></tr><tr><td>

Send notifications

</td><td>

Sends notifications to the assigned users when the survey is published if there is an active notifications setup. Configure the form to see the field.

</td></tr><tr><td class="sub-head" colspan="2">

Other Options

</td></tr><tr><td>

Sample Metric

</td><td>

A metric of the current survey that you can include as an image in the email or invitation sent to a survey user. When the survey user clicks the image in the email or while previewing the HTML body, the entire survey is available to be taken.**Note:** You cannot edit or delete a metric that is selected in this field.

</td></tr><tr id="tr_SurveySignature"><td>

Signature

</td><td>

Acknowledgement by a survey recipient of requirements, admonitions, or policies related to the survey. The signature may require the recipient to select a check box or to type in a full signature to verify having read these assertions. You can display assertions without requiring a signature. Select an existing signature from the list or click **New** to create a new one. The signature form contains these fields: -   **Name**: Descriptive name for this signature.
-   **Signature type**: Type of signature required. The selections are **Check box**, **Full name**, or **Assertion only**. If **Assertion only** is selected, no signature is required to submit the survey.
-   **Assertion**: Text you want to display to recipients.
 By default, a property called **Require authentication for user signature** \(**com.snc.assessment.signature\_authentication**\) requires users to authenticate when providing a full name signature.

</td></tr><tr id="tr_SurveySchedule"><td>

Schedule period

</td><td>

Option that determines how often a user can take the same survey and whether the system generates survey instances on a schedule.**Note:** If you use a trigger condition for a survey, ensure the schedule period is set to **No Limit**. Trigger conditions use a different method to regulate how often users can receive survey instances.

</td></tr><tr><td>

Do not show survey introduction notes

</td><td>

Check box to skip the introduction notes when a survey is launched. This functionality is applicable in both the ServiceNow AI Platform and Service Portal product versions.

</td></tr><tr><td>

Pagination setting for Service Portal view

</td><td>

The setting on which the pagination is based for desktop or tablet view in Service Portal.-   Category: default
-   Question: 1 question per page \(automatic for mobile\)
-   None: no pagination
 **Note:** This field is displayed only when Service Portal is installed.

</td></tr><tr><td>

One Click Survey

</td><td>

Enables a One Click survey in Service Portal.**Note:** This option can be selected if the **Pagination setting for Service Portal view** is set to `None`.

</td></tr><tr><td>

Source Table

</td><td>

Table whose field is used as a dynamic value for a question in a triggered survey.**Note:** When you select a source table, ensure that its relevant field is selected as **Source Field** value of a metric.

</td></tr><tr><td>

Chat Survey

</td><td>

Option to validate if survey questions are supported in a chat survey. Enables conversational questionnaires \(pre-chat and post-chat surveys\) in the chat client. Also enables you to map chat context variables to survey questions. For information on a chat survey in ITSM Virtual Agent, see [Surveys in ITSM Virtual Agent](../concept/survey-virtual-agent.md).**Note:** This field is available only when the Glide Conversation Server plugin \(com.glide.cs\) is activated.

</td></tr><tr><td>

Outlook Actionable Message

</td><td>

Includes an embedded survey in the survey email notification. After you select this check box and save the survey, a validation is run to ensure all survey questions are supported. **Note:** This field is available only when the Outlook Actionable Messages\(sn\_ms\_oam\) plugin is installed.

</td></tr><tr><td>

Allow Sentiment Analysis

</td><td>

Enables sentiment analysis for this survey.

</td></tr><tr><td class="sub-head" colspan="2">

Introduction &amp; End Notes

</td></tr><tr><td>

Introduction

</td><td>

Introductory content to display on survey questionnaires. Consider adding a company logo, a welcome message, background information about the survey, or instructions.

</td></tr><tr><td>

End note

</td><td>

End note that appears when someone submits a survey questionnaire. Consider adding a thank you message, follow-up instructions, or other applicable information.

</td></tr><tr><td class="sub-head" colspan="2">

Related Links

</td></tr><tr><td>

Enable Public AccessRemove Public Access

</td><td>

Link that enables/disables the survey as a public survey. No login is required to take a public survey \(including a survey with a trigger condition\) and users or non-users can respond anonymously. For completed public surveys, the **Assigned to** field value is Guest. **Note:** You can use the **View Survey URL** related link to share the URL with users.

</td></tr><tr><td>

View Responses

</td><td>

Link that opens the list of [responses](../concept/c_SurveyResults.md) for this survey. This related link is available only if there are results for the survey.

</td></tr><tr><td>

View Scorecard

</td><td>

Link that opens the [scorecard](t_ViewAScorecard.md) for this survey. This related link is available only if there are results for the survey.

</td></tr><tr><td>

View Survey URL

</td><td>

Link that opens a dialog box that displays a [URL](../concept/c_SurveyURLs.md) for this survey. The URL is useful for sharing a public survey.This related link is available only if the **Active** check box is selected. The URL does not work until the survey definition is published.

</td></tr><tr><td>

Show Benchmarks

</td><td>

Opens the Benchmarks Dashboard that provides visibility into your key performance indicators \(KPIs\) and trends.**Note:**

-   This related link is available only for survey\_admin, assessment\_admin and survey\_reader with bm\_viewer role.
-   You must opt in to Benchmarks to view the dashboard. See Enable Benchmarks
-   This is applicable only for a published survey.


</td></tr><tr><td>

Create Improvement Initiative

</td><td>

Opens the Improvement Initiative window to create an improvement initiative record that helps in improving the performance of the survey.**Note:**

-   This related link is available only for the survey\_admin and assessment\_admin role. A survey\_reader can only view the created improvement initiative records.
-   You should activate the Continual Improvement Management plugin \(com.sn\_cim\).


</td></tr><tr><td>

Retry Sentiment Analysis

</td><td>

Checks all survey instances of this survey that do not have sentiment analysis data and sends them for analysis.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Trigger Condition

</td><td>

Displays all the trigger conditions associated with the survey.

</td></tr><tr><td>

Survey Responses

</td><td>

Displays all the responses associated with the survey.

</td></tr><tr><td>

Metric Categories

</td><td>

All [survey categories](../concept/c_SurveyCategory.md) for this survey.

</td></tr><tr><td>

Survey Users

</td><td>

All [survey users](../concept/c_SurveyUsersAndGroups.md) who are authorized to take this survey. If no users are listed, any user can take this survey.

</td></tr><tr><td>

Assessment Instances

</td><td>

All [survey instances](t_ViewSurveyInstance.md) for this survey. Configure the form to add this related list to see it.

 **Note:** If you add a related list to the form, use list control to omit the **New** button. The system generates survey instances to produce functional surveys.

</td></tr><tr><td>

Improvement Initiatives

</td><td>

Displays improvement initiatives associated with the survey.**Note:** This related list is available only when there is at least one improvement initiative record.

</td></tr><tr><td>

Survey Recipients Lists

</td><td>

Recipients lists that are added to the survey.

</td></tr></tbody>
</table>4.  Save the record.


**Parent Topic:**[Survey definitions](../concept/c_SurveyDefinitions.md)

**Related topics**  


[Survey trigger conditions](../concept/c_TriggerConditions.md)

[Publish a survey](t_PublishASurvey.md)

[bundle-platadm.c_ScheduleEvents]

