---
title: Survey URLs
description: You can distribute a survey by giving survey users a survey URL.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey URLs

You can distribute a survey by giving survey users a survey URL.

Survey administrators can obtain one of the following types of URLs.

-   A general URL for a survey, which users can open to take the survey questionnaire. The following process occurs.
    -   When someone opens the URL, the system ensures that the person is logged in. It then searches for an instance of the associated survey that is assigned to the logged-in user.
    -   If a survey instance is found, the appropriate action occurs based on the **State** of the survey instance \(see table\). If there are multiple active survey instances \(**Ready to take** or **In progress**\), the instance with the earliest due date opens.
    -   If no survey instance is found, the system creates a new instance for the survey, assigns it to the user, and opens the survey questionnaire.
-   A URL for a specific survey instance, which the assigned user can open to take the survey questionnaire. The following process occurs.
    -   When someone opens the URL, the system ensures the person is logged in as the user the survey instance is assigned to. Only the assigned user can access the survey questionnaire.
    -   The appropriate action occurs, depending on the **State** of the survey instance \(see table\).

<table id="table_nc2_rlj_np"><thead><tr><th>

Survey instance state

</th><th>

Action upon opening URL

</th></tr></thead><tbody><tr><td>

**Ready to take**: User has not saved any responses.

</td><td>

The survey questionnaire appears for the user to begin. The user can save or submit responses.

</td></tr><tr><td>

**In progress**: User has saved at least one response.

</td><td>

The survey questionnaire appears for the user to continue. Any previously saved responses are displayed. The user can save or submit responses.

</td></tr><tr><td>

**Complete**: User has submitted all required responses.

</td><td>

If the schedule period is **No Limit** or if the period restriction has expired, the survey questionnaire for a new survey instance appears for the user to begin. If the schedule period restricts the number of times a user can take the same survey, and the period restriction has not expired since the user last completed survey, an error message appears.

</td></tr></tbody>
</table>If someone opens a URL for an unpublished or deactivated survey, an error message appears.

-   **[Obtain and distribute a general survey URL](../task/t_ObtainAGeneralSurveyURL.md)**  
You can distribute a general survey URL to allow any eligible user to open a survey questionnaire.
-   **[Deactivate auto-notification for surveys](../task/t_DeactivateAutoNotifyForSurveys.md)**  
Deactivate an auto-notification to avoid a problem that causes a second system-generated email notification being sent to a user.
-   **[Obtain a survey instance URL](../task/t_ObtainASurveyInstanceURL.md)**  
You can distribute a survey instance URL to allow the assigned user to open a survey questionnaire.
-   **[Test a survey URL](../task/t_TestTheSurveyURL.md)**  
When there are survey users associated with a survey, the survey is restricted so only those users can use the survey URL. You can test the survey URL to ensure it is restricted.

**Parent Topic:**[Survey distribution](c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](email-notification-for-surveys.md)

[Send survey invitations to users](../task/t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](../task/define-recipient-list.md)

[Add a recipients list to a survey](../task/add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](../task/embed-survey-in-outlook-email.md)

[Enable localization for a survey](../task/enable-localization-survey.md)

[Create a survey module](../task/t_CreatingASurveyModule.md)

[Sharing surveys](c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](../task/take-survey-connect-chat.md)

