---
title: Survey administration
description: Survey administrators—users with the survey\_admin role—create and maintain surveys and configure how they are distributed and published. Surveys on Service Portal are also supported.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey administration

Survey administrators—users with the survey\_admin role—create and maintain surveys and configure how they are distributed and published. Surveys on Service Portal are also supported.

Survey administration includes the following procedures.

-   Create, customize, and publish surveys.
-   Write and maintain survey questions.
-   Define trigger conditions for when surveys are sent to users, such as when an incident closes.
-   Maintain surveys and survey questions as the organization's needs change.

To set up surveys in [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US), you must first install Service Portal and then [Create and edit a page using the Service Portal Designer](https://www.servicenow.com/docs/access?context=t_ConfigureAPage&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) on the page. The base system includes the Survey widget.

-   **[View survey reports](../task/view-survey-overview.md)**  
Use the Survey Overview dashboard to view various survey reports, such as Surveys by Metric Type and State.
-   **[Survey designer](../concept/c_SurveyDesigner.md)**  
Users with the survey\_admin role can use the survey designer. The survey designer lets you create survey categories and questions, configure the details, and publish the survey to specific users or groups.
-   **[View a survey instance](../task/t_ViewSurveyInstance.md)**  
A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.
-   **[Survey users and groups](../concept/c_SurveyUsersAndGroups.md)**  
Survey users and survey user groups help survey administrators control who can take a survey.
-   **[Copy a survey](../task/copy-survey.md)**  
Create a copy of a survey with at least one category to reduce the effort of creating another survey with similar data.
-   **[Publish a survey](../task/t_PublishASurvey.md)**  
You must publish a survey to enable people to receive and complete survey instances.
-   **[Customize the appearance of a survey](../task/t_CustomizingAppearance.md)**  
As an assessment and survey administrator, set properties to customize the color of various elements on the questionnaires.
-   **[Survey definitions](../concept/c_SurveyDefinitions.md)**  
A survey definition is the root record upon which a survey is built.
-   **[Create a survey designer template question](../task/t_CreateASurveyDesignerTemplateQ.md)**  
You can create a question that uses choice lists from a template.
-   **[Survey questions](../concept/c_SurveyQuestion.md)**  
Survey questions appear on survey questionnaires for the associated survey definition.
-   **[Survey trigger conditions](../concept/c_TriggerConditions.md)**  
Trigger conditions specify when to send a particular survey and the persons to send it to.
-   **[Survey distribution](../concept/c_SurveyDistribution.md)**  
There are several ways for survey administrators to distribute surveys to users.
-   **[Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md)**  
Outlook actionable messages plugin enables users to respond to the survey from within the Microsoft Outlook application.
-   **[Sentiment analysis for surveys](../concept/sentiment-analysis.md)**  
You can use sentiment analysis to determine whether user responses for a survey are considered positive, negative, or neutral.
-   **[Surveys in Service Portal and the Now Mobile app](../concept/c_SurveyServicePortal.md)**  
If you've installed Service Portal, you can use the My Assessments and Surveys widget in Service Portal. Users can view surveys in Service Portal. Service Portal also supports surveys for users on mobile devices that have the Now Mobile app installed. The My Assessments and Surveys widget is available by default on the Service Portal home page.
-   **[Surveys in ITSM Virtual Agent](../concept/survey-virtual-agent.md)**  
You can use surveys in ITSM Virtual Agent to collect survey responses from users through conversational questionnaires \(pre-chat and post-chat surveys\) in the chat client.
-   **[Legacy survey migration](../concept/c_MigrateSurveys.md)**  
Users with the survey\_admin role can migrate legacy survey data to create copies of legacy surveys and their related records in assessment tables. The Survey Management application, which is built on the assessment engine, is available as an alternative to legacy surveys.

**Parent Topic:**[Using surveys](../concept/using-surveys.md)

