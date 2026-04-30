---
title: Surveys in Service Portal and the Now Mobile app
description: If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view surveys in Service Portal. Service Portal also supports surveys for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Surveys in Service Portal and the Now Mobile app

If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view surveys in Service Portal. Service Portal also supports surveys for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.

## Surveys in Service Portal

To create an intuitive interface for your users, you can set up surveys in [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) . Activate Service Portal to view the My Assessments and Surveys widget, which appears on the Service Portal home page.

To learn more about activating Service Portal, see [Activate Service Portal](https://www.servicenow.com/docs/access?context=activate-service-portal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

To learn more about configuring a widget, see [configure widget instances](https://www.servicenow.com/docs/access?context=c_ConfigureWidgetInstances&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) .

To configure a survey widget on a Service Portal page, press the CTRL key, right-click the widget heading, and select **Instance Options**.

<table id="table_afm_bdv_jx"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max records

</td><td>

Maximum number of surveys to list in the widget on the Service Portal home page. Click the **View all** link to view all surveys.Default: **5**

</td></tr><tr><td>

Title of the widget

</td><td>

Text that appears in the title bar of the surveys widget.Default: **My Assessments and Surveys**

</td></tr></tbody>
</table>![My Assessments and Surveys page.](../../assessments/images/ecs-my-assessments-surveys-widget.png "My Assessments and Surveys widget on the Service Portal home page")

## Surveys in the Now Mobile app

Users can view and take the surveys on mobile devices using the My Assessments and Surveys applet launcher that is available by default in the Now Mobile app.

When you assign a survey to a user an email notification about taking the survey is sent to the user. If users have installed the Now Mobile app, a mobile push notification is also sent on mobile devices. Tapping the notification opens an introduction page for a survey in the Mobile Employee Service Portal in the Now Mobile app. The page shows a **Get started** link. The introduction page and the **Get started** link are available only if the related settings are enabled. Users can tap the link to view and take the survey. You can activate push notifications by setting the **glide.sg.universal\_links.enabled** system property to **true**.

**Note:** A push notification doesn't apply for a triggered survey. For a triggered survey, an event is inserted in the event queue. The event can be configured to determine whether to send a notification or not.

![Mobile survey.](../../assessments/images/AssessmentsandSurveysInNowMobilApp.png "My Assessments and Surveys applet on a mobile device")

**Note:** In the Zurich version, you now see the assessments and surveys assigned in the card view instead of the item view. If you customize the styles of the legacy card item views in older versions of  Assessments and Surveys, the card continues to appear in the item view even after you upgrade to Zurich. You can view the new card view in Zurich only if no customizations were made to the legacy cards.

When users open a survey either in Service Portal or the Now Mobile app, the surveys provide the following features:

-   A survey page shows breadcrumb navigation on the Service Portal. Users can click the links in the breadcrumb to navigate to previous pages or a home page. For example, clicking the **My Surveys** link in the breadcrumb navigates users to a page, which shows a list of all the surveys.
-   When the survey is in progress, the progress bar, which is available on each page of the survey, shows the progress in percentage. The percentage of completion is based on the pages on the survey. For example, suppose that there are three pages of a survey. The third page shows 66% completion of the survey. But giving a response to one of the questions on the third page opens a new question on a separate page, which is the fourth page. The fourth page shows the progress of the survey as 75% completed, which affects the overall progress and page indicators. Users can see the pagination \(total number of pages\) for the entire survey as well as the current page that the users are on. To hide or show this progress bar, you can use the **sn\_portal\_surveys.sp\_survey.show\_progress\_bar** property.
-   Each user response is saved automatically when users move to the next page in the survey. If users don't answer the required survey questions before clicking **Next**, the page shows an error message at the top for all required and unanswered questions. This error message helps users find the exact location of the unanswered and required question. Any question that is not required and is not responded to before clicking **Next** is considered answered. The question is counted as completed.
-   When the details of a survey question contain more than four or five lines of text, the text after these lines disappears. In such cases, users can see the complete details by clicking the **Show more** link. Users can go back to the default behavior by clicking the **Show less** link.
-   For a question that has the answer options of **Yes**, **No**, and **Not Applicable**, the **Not Applicable** option appears last in the list of options. The **Not Applicable** option can be configured while creating a question.

-   When the survey users leave the survey without submitting it, they can start the survey later from the same page where they left off in the previous session.

**Note:** For mobile users, the pagination is always by question for surveys. For more information about pagination settings, see [Configure a survey in the survey designer](../task/t_ConfigSurveyInSurveyDesgnr.md).

## One Click survey

A One Click survey has no introduction page in Service Portal. This survey doesn’t have the **Submit** and **Cancel** buttons in the desktop and iPad view.

**Note:**

-   The One Click Survey is not supported in the mobile device view.
-   The **One Click Survey** field should be selected in the survey definition.
-   When the public access is enabled for a One Click survey, a user can submit the survey without having to log in.
-   When the public access is enabled for a survey, you can't configure a signature or an attachment for the survey.
-   For a published public survey, the Signature field is hidden and you can’t add an attachment.

A kiosk survey is a One Click survey with only one question of any of the following types:

-   Image Scale
-   Choice
-   Likert Scale
-   Numeric Scale
-   Yes/No

When users click the answer for the kiosk survey question in Service Portal, the survey is submitted, and the end note is displayed on the same page that contains the survey questions. The kiosk survey becomes read-only after it's clicked.

**Note:**

-   A kiosk survey doesn't have any **Submit** or **Cancel** buttons.
-   A kiosk survey can't have a signature, dependent questions, or additional information.
-   A kiosk survey doesn't display introduction notes.

## URI parameters for One Click survey

Pass these URI parameters through the createAssessment\(\) API to store their values in the asmt\_assessment\_instance table for both platform view and Service Portal view.

|Parameter|Description|
|---------|-----------|
|**sysparm\_refresh\_interval**|Refresh the time, in seconds, after the survey submission to create another instance. For example, sysparm\_refresh\_interval=5.|
|**sysparm\_trigger\_table**|Location that is stored as the **Trigger Table** field in the asmt\_assessment\_instance table. For example, sysparm\_trigger\_table=incident.|
|**sysparm\_trigger\_id**|Location sys\_id that is stored as the **Trigger ID** field in the asmt\_assessment\_instance table. For example, sysparm\_trigger\_id=1c741bd70b2322007518478d83673af3.|
|**sysparm\_kiosk**|When set to **true**, both the sysparm\_trigger\_table and sysparm\_trigger\_id parameters should be specified. This parameter is required for kiosk requests. For example, sysparm\_kiosk=true.|

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

[Surveys in ITSM Virtual Agent](survey-virtual-agent.md)

[Legacy survey migration](c_MigrateSurveys.md)

[Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

[Create and edit a page using the Service Portal Designer](https://www.servicenow.com/docs/access?context=t_ConfigureAPage&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

[Survey designer](c_SurveyDesigner.md)

[Configure a survey in the survey designer](../task/t_ConfigSurveyInSurveyDesgnr.md)

