---
title: Survey Instance form
description: Description of the field values for the on the Survey Instance form.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey Instance form

Description of the field values for the on the Survey Instance form.

<table id="table_kpz_q5j_np"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated record number.

</td></tr><tr><td>

Metric type

</td><td>

Survey definition this survey instance was created from. Survey definitions are stored on the Assessment Instance table, and the field label on that table is **Metric type**.

</td></tr><tr><td>

Due date

</td><td>

Date by which the survey instance should be completed. The system populates the due date based on the **Assessment duration** of the associated survey definition, which is set to 14 days by default.The survey due date is not enforced in the base system. If you want to enforce the due date, consider using a workflow or other mechanism to send survey recipients reminders when a survey is overdue.

 **Note:** By default, the system runs the **Cancel Expired Assessments** script every 30 days to cancel expired survey, assessment, and quiz instances that are in the Work in progress or Ready to take states.

</td></tr><tr><td>

State

</td><td>

State of the survey instance.

</td></tr><tr><td>

Assigned to

</td><td>

User this survey instance is assigned to. This field becomes read-only when the state is In progress, Complete, or Canceled.

</td></tr><tr><td>

Domain

</td><td>

Domain associated with the instance.

</td></tr><tr><td>

Expiration date

</td><td>

Date on which the assigned user can receive a new instance of the same survey definition. The system automatically populates the expiration date based on the **Schedule period** of the associated survey definition.

</td></tr><tr><td colspan="2">

Related Link

</td></tr><tr><td>

View User's Response

</td><td>

Shows a read-only version of the survey responses completed by the user.

</td></tr><tr><td>

Retry Sentiment Analysis

</td><td>

Sends the survey instances for sentiment analysis.**Note:** This link is available only if any sentiment analysis result is not available for this instance under **Survey** &gt; **Question Sentiment Results**

</td></tr><tr><td colspan="2">

Related List

</td></tr><tr><td>

Assessment Instance Questions

</td><td>

All instance question records, which store user response values for each question on the survey questionnaire. The following columns are relevant to surveys:-   **Category**: Displays the survey categories the questions belong to.
-   **Metric**: Displays the survey questions.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

**Related topics**  


[View a survey instance](../task/t_ViewSurveyInstance.md)

