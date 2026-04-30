---
title: Add a recipients list to a survey
description: Send the survey invites to targeted sets of users by adding a recipients list to a survey.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a recipients list to a survey

Send the survey invites to targeted sets of users by adding a recipients list to a survey.

## Before you begin

Role required: admin or survey\_admin

Recipients lists should be pre-defined in the Recipients Lists submodule. For more information on defining recipients lists, see [Define a recipients list for surveys](define-recipient-list.md).

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition.

3.  Perform any of the following steps.

<table id="choicetable_jnl_df2_5fb"><thead><tr><th align="left" id="d424191e84">

Option

</th><th align="left" id="d424191e87">

Description

</th></tr></thead><tbody><tr><td id="d424191e93">

**From Platform**

</td><td>

1.  Under the **Survey Recipients Lists** related list, click **New**.
2.  In the Survey Recipients Lists form, from the **Recipients List** list, select the required recipients list.
3.  Click **Submit**.


</td></tr><tr><td id="d424191e126">

**From Survey Designer**

</td><td>

1.  Under the **Availability** tab, for the **Accessible By** field, select **Specific users**.
2.  In the **Add recipients lists** list, select the required recipients list.
3.  To send the survey to users, click **Save and Publish**.


</td></tr></tbody>
</table>4.  To send survey invites to all survey users and recipients lists, click **Send Invitations**.

    **Note:**

    -   The **Send Invitations** UI action is available when there is at least one recipients list or survey user for the survey.
    -   If a user is available in the **Survey Users** related list and multiple recipients lists, the survey invite is sent only once to the user.

**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Send survey invitations to users](t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Embed a survey within the Outlook email client](embed-survey-in-outlook-email.md)

[Enable localization for a survey](enable-localization-survey.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Create a survey module](t_CreatingASurveyModule.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](take-survey-connect-chat.md)

