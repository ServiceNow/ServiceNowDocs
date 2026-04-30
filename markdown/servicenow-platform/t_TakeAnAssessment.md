---
title: Take an assessment
description: Take the assessments assigned to you from the assessment and survey queue.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Take an assessment

Take the assessments assigned to you from the assessment and survey queue.

## Before you begin

Role required: none

## About this task

An assessment card displays the assessment name, state, due date, and associated incident number. Click the card to take the assessment when you're ready.

You must answer every required question, indicated by a red asterisk, before you can submit the assessment as complete. If you start to take an assessment but can't complete it, save your responses and return to it later. When you've answered all the questions and you're happy with the responses, submit the assessment.

**Note:** The expired assessments and surveys no longer appear in the **My surveys** widget and the **My Assessments and Surveys list** page.

By default, you can't modify your answers to an assessment after submission. However, if the administrator has configured an assessment to allow retakes, you can edit your answers and resubmit the questionnaire. Completed assessments configured for retake remain in the queue until their due date and display Modify Assessment at the top of the card. Click the card to modify the assessment.

**Note:** If you don’t have access to the assessable record for which an assessment is created, the associated record number isn't displayed. You can still take the assessment.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Assessments &amp; Surveys**.

    **Note:** Users with the assessment\_admin role can display other users' assessments and surveys in addition to their own. Use the **Show all** and **Show assigned to me** related links to show and hide assessments and surveys. Click a card assigned to another user to open the associated metric type or survey definition.

2.  On the assessment card, note the due date.

    **Note:** Depending on the configuration, you may receive email notifications to remind you of the due date.

3.  Click the card to open the questionnaire.

    Assessment questionnaires are arranged in sections: first by record, then by category. Each record appears as a section title. Questions for the record appear underneath the record, grouped by category. Each category appears as a subsection underneath the record name. Click the collapse icon \(![Collapse icon](../images/CollapseIcon.png)\) or expand icon \(![Expand icon](../images/ExpandIcon.png)\) to hide or show the questions in a category, or all the categories and questions for a record. Colored bars indicate the status of each question.

    ![Assessment questionnaire form](../images/AssessmentQuestionnaireForm.png)

4.  Answer each question to the best of your ability.

    Point to a question for more information.

    ![Tooltip for an assessment metric](../images/AssessmentMetricTooltip.png)

    If you're unsure of how to respond to a question or if a question doesn't apply to a particular record, select **Not Applicable**, if available.

5.  Read any assertions present at the end of the assessment and acknowledge with a signature, if required.

    A signature can require you to select a check box or authenticate your full name, which the system displays in a read-only field. You can't submit your answers to the assessment until you provide the required signature.

6.  Save or submit the assessment.

    -   **Save**: Saves your responses without submitting them. You can close the questionnaire and access it later from your queue.
    -   **Submit**: Submits the completed assessment when you're finished.
7.  If prompted, enter your user name and password to verify your full name signature.

    If all the questions are answered with valid values, a`success` message appears. If the system detects an unanswered required question or invalid response, the assessment isn't submitted, and a message appears at the top of the questionnaire explaining the error. Questions with problems are temporarily highlighted.

    ![Error messages for invalid responses](../images/AssessmentsInvalidValue.png)

8.  You can modify your responses to the assessment until its due date.

    To update your answers and resubmit an assessment that permits retakes, click the card to modify it.


-   **[Assessments in Service Portal and the Now Mobile app](../concept/assessment-service-portal-and-now-mobile-app.md)**  
If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view and take assessments in Service Portal. Service Portal also supports assessments for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.
-   **[Assessment questionnaires](../concept/c_AssessmentQuestionnaires.md)**  
In the assessment process, users complete assessment questionnaires on topics of interest to provide subjective data for future business decisions.

**Parent Topic:**[Using assessments](../concept/using-assessments.md)

**Related topics**  


[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

[Survey definitions](../../survey-administration/concept/c_SurveyDefinitions.md)

