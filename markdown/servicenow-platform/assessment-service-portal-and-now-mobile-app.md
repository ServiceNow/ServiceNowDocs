---
title: Assessments in Service Portal and the Now Mobile app
description: If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view and take assessments in Service Portal. Service Portal also supports assessments for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Take an assessment, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessments in Service Portal and the Now Mobile app

If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view and take assessments in Service Portal. Service Portal also supports assessments for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.

## Assessments in Service Portal

To create an intuitive interface for your users, you can set up assessments in Service Portal. Activate Service Portal to view the My Assessments and Surveys widget, which appears on the Service Portal home page.

To learn more about activating Service Portal, see Activate Service Portal.

To learn more about configuring a widget, see configure widget instances .

To configure an Assessments and Surveys widget on a Service Portal home page, press the CTRL key, right-click the widget heading, and select **Instance Options**.

<table id="table_pxd_wmd_15b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max records

</td><td>

Maximum number of assessments to list in the widget on the Service Portal home page. Users can click the **View all** link to view all assessments.

Default number of assessments: **5**

</td></tr><tr><td>

Title of the widget

</td><td>

Text that appears in the title bar of the survey widget.

 Default title: **My Assessments and Surveys**

</td></tr></tbody>
</table>![My Assessments and Surveys widget on the Service Portal home page.](../images/ecs-my-assessments-surveys-widget.png "My Assessments and Surveys widget on the Service Portal home page")

## Assessments in the Now Mobile app

Your users can view and take the assessments on mobile devices using the My Assessments and Surveys applet launcher that is available by default in the Now Mobile app.

When you assign an assessment to a user, an email notification about taking the assessment is sent to the user. If users installed the Now Mobile app, a mobile push notification is also sent on mobile devices. Tapping the notification opens an introduction page for an assessment in the Mobile Employee Service Portal in the Now Mobile app. The page displays a **Get started** link. The introduction page and the **Get started** link are available only if the related settings are enabled. Users can tap the link to view and take the assessment. You can activate push notifications by setting the **glide.sg.universal\_links.enabled** system property to **true**.

![My Assessments and Surveys applet on a mobile device.](../images/AssessmentsandSurveysInNowMobilApp.png "My Assessments and Surveys applet on a mobile device")

**Note:** In the Australia release, you now see the assessments and surveys assigned in the card view instead of the item view. If you customize the styles of the legacy card item views in older versions of Assessments and Surveys, the card continues to appear in the item view even after you upgrade to Australia. You can view the new card view in Australia only if no customizations were made to the legacy cards.

When users open an assessment either in Service Portal or the Now Mobile app, the assessment provides the following features:

-   An assessment page shows breadcrumb navigation on the Service Portal. Users can click the links in the breadcrumb to navigate to previous pages or a home page. For example, clicking the **My Surveys** link in the breadcrumb navigates users to a page, which shows a list of all the assessments.
-   When the assessment is in progress, the progress bar, available on each page of the assessment, shows the progress in percentage. The percentage of completion is based on the number of pages in the assessment. For example, suppose that there are three pages in the assessment. The third page shows 66% completion of the assessment. But giving a response to one of the questions on the third page opens a new question on a separate page, which is the fourth page. The fourth page shows the progress of the assessment as 75% completed, which affects overall progress and page indicators. Users can see the pagination - total number of pages - for the entire assessment as well as the current page that the users are on. To hide or show this progress bar, you can use the **sn\_portal\_surveys.sp\_survey.show\_progress\_bar** property.
-   Each user response is saved automatically when users move to the next page in the assessment. If users don't answer the required assessment questions before clicking **Next**, the page shows an error message at the top for all required and unanswered questions. This error message helps users find the exact location of the unanswered and required question. Any question that is not required and is not responded to before clicking **Next** is considered answered. The question is counted as completed.
-   When the details of an assessment question contains more than four or five lines of text, the text after these lines disappears. In such cases, users can see the complete details by clicking the **Show more** link. Users can go back to the default behavior by clicking the **Show less** link.
-   For a question that has the answer options of **Yes**, **No**, and **Not Applicable**, the **Not Applicable** option appears last in the list of options. The **Not Applicable** option can be configured while creating a question.
-   Your users can take assessments for multiple incident records generated. For example, suppose that users have two incident records generated. The user can take an assessment for both the incident records generated using the same assessment instance.
-   When the assessment users leave the assessment without submitting it, they can start the assessment later from the same page where they left off in the previous session.

    **Note:** For mobile users, the pagination is always by question for assessments.


**Parent Topic:**[Take an assessment](../task/t_TakeAnAssessment.md)

**Related topics**  


[bundle-platux.activate-service-portal]

