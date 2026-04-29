---
title: Survey Designer Configuration form
description: Description of the field values for the Survey Designer Configuration form.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey Designer Configuration form

Description of the field values for the Survey Designer Configuration form.

<table id="table_dwb_gwh_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Select the check box to enable the distribution of this survey to recipients.

</td></tr><tr><td>

Survey Owners

</td><td>

Owners of the survey. You can add a user with the survey\_creator, survey\_admin, or assessment\_admin role.

</td></tr><tr><td>

Anonymize responses

</td><td>

Select the check box to collect survey responses anonymously. Recipients are not listed with survey results. When a user submits a survey, the system clears the **Assigned to** field for the associated survey instance. Also, survey responses for anonymous surveys do not contain Assigned to values.**Note:** The **Assigned to** field is cleared. However, each response record includes the **Created By** and **Updated By** fields that are accessible to users with the survey\_admin role.

</td></tr><tr><td>

Description

</td><td>

Description of this configuration or the survey to which it is attached.

</td></tr><tr><td>

Do not show survey introduction notes

</td><td>

Check box to skip the introduction notes when a survey is launched. This functionality is applicable in both the ServiceNow AI Platform and Service Portal product versions.

</td></tr><tr><td>

Introduction

</td><td>

Introductory content to display on surveys. You can add a welcome message or background information about the survey.

</td></tr><tr><td>

Signature

</td><td>

Acknowledgement by a survey recipient of requirements, admonitions, or expectations related to a survey.

</td></tr><tr><td>

Return URL

</td><td>

Destination address of a web page that is presented to users after they submit a completed survey. When a return URL is configured, the **End note** content does not appear.

</td></tr><tr><td>

End note

</td><td>

Content that is displayed to recipients after they submit a completed survey. You can add a thank you message, follow-up instructions, or other applicable information. End notes are not displayed if a **Return URL** is specified.

</td></tr><tr><td>

Public Survey

</td><td>

Enables public access to the survey. No login is required to take a public survey and users or non-users can respond anonymously. For completed public surveys, the **Assigned to** field value is Guest.**Note:** This check box is available only after you save the survey.

</td></tr><tr><td>

Survey Publish URL

</td><td>

Specifies a URL of the survey that can be shared with users.**Note:** This field is available only after you publish the survey.

</td></tr><tr><td>

Sample metric

</td><td>

Specifies the metric that appears as a sample in emails sent to users.

</td></tr><tr><td>

Pagination setting for Service Portal view

</td><td>

Specify how the user will see pages on the desktop or tablet view in Service Portal.-   **Category**: Display each category on a separate page.
-   **Question**: Display each question on a separate page. This happens for mobile regardless of this setting.
-   **None**: All items on a single page—no pagination

Default: **Category** **Note:** This field appears only when Service Portal is installed.

</td></tr><tr><td>

Chat Survey

</td><td>

Option to validate if survey questions are supported in a chat survey. Enables conversational questionnaires \(pre-chat and post-chat surveys\) in the chat client. Also enables you to map chat context variables to survey questions. For information on a chat survey in ITSM Virtual Agent, see [Surveys in ITSM Virtual Agent](../concept/survey-virtual-agent.md) **Note:** This field is available only when the Glide Conversation Server plugin \(com.glide.cs\) is activated.

</td></tr><tr><td>

One Click Survey

</td><td>

Enables a One Click survey in Service Portal.**Note:** This option can be selected if the **Pagination setting for Service Portal view** is set to `None`.

</td></tr><tr><td>

Source Table

</td><td>

Table whose field is used as a dynamic value for a question in a triggered survey.**Note:** When you select a source table, ensure that its relevant field is selected as **Source Field** value of a metric.

</td></tr><tr><td>

Allow Sentiment Analysis

</td><td>

Enables sentiment analysis for this survey.

</td></tr><tr><td>

Duration

</td><td>

Amount of time that recipients are given to complete this survey, starting from the time that the survey is generated. The default duration is 14 days.

</td></tr><tr><td>

Outlook Actionable Message

</td><td>

Includes an embedded survey in the survey email notification. After you select this check box and save the survey, a validation is run to ensure all survey questions are supported. **Note:** This field is available only when the Outlook Actionable Messages\(sn\_ms\_oam\) plugin is installed.

</td></tr></tbody>
</table><table id="table_q1z_vr2_5fb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Accessible by

</td><td>

Defines who can access the survey. Possible values are-   Anyone: Accessible by anyone with the survey link.
-   Specific users: Accessible by specified users.

</td></tr><tr><td>

Survey groups only

</td><td>

If selected, a survey is available for survey groups only.**Note:** This field is displayed only if the **Accessible by** is `Specific users`.

</td></tr><tr><td>

Add group users

</td><td>

Group users for whom the survey is available.**Note:** This field is displayed only if the **Accessible by** is `Specific users`.

</td></tr><tr><td>

Add users

</td><td>

Users for whom the survey is available.**Note:** This field is displayed only if the **Accessible by** is `Specific users`.

</td></tr><tr><td>

Add recipients lists

</td><td>

Recipients lists for whom the survey is available.**Note:** This field is displayed only if the **Accessible by** is `Specific users`.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

