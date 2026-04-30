---
title: Send survey invitations to users
description: You can send survey invitations using the Assign Survey or Send Invitations buttons on the Survey Definition form.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send survey invitations to users

You can send survey invitations using the **Assign Survey** or **Send Invitations** buttons on the Survey Definition form.

## Before you begin

Role required: admin or survey\_admin

## About this task

Use the **Send Invitations** button to immediately assign survey instances to each survey user that is listed in the survey definition. Use the **Assign Survey** button to assign a survey instance to any one user at a time.

Each of the buttons generates survey instances assigned to the appropriate users. In addition, if the instance is configured to send email, the system generates survey notifications. For either button to be available, the survey definition must meet all of the following conditions.

-   **Active** check box is selected.
-   **State** is **Published**.
-   Survey is associated with at least one question.

**Note:** You \(or a trigger\) can send more than one instance of a survey to a user at any time.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Select an active, published survey.

3.  Complete one of the following actions.

<table id="choicetable_yzz_24g_45"><tbody><tr><td id="d605782e123">

**Assign a survey to users listed in the Survey Users related list**

</td><td>

Click **Send invitations**.

</td></tr><tr><td id="d605782e135">

**Assign a survey to any user**

</td><td>

Click **Assign Survey** and select one or more users, and then click **OK**.

</td></tr></tbody>
</table>    The system creates a survey instance assigned to the user or users, assuming the user is eligible to receive a new survey instance. When you use the **Assign Survey** button, the selected user is not saved as a survey user.


**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Add a recipients list to a survey](add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](embed-survey-in-outlook-email.md)

[Enable localization for a survey](enable-localization-survey.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Create a survey module](t_CreatingASurveyModule.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](take-survey-connect-chat.md)

