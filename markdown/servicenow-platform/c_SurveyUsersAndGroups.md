---
title: Survey users and groups
description: Survey users and survey user groups help survey administrators control who can take a survey.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey users and groups

Survey users and survey user groups help survey administrators control who can take a survey.

Survey administrators can restrict a survey so that only specified users can access it unless a survey administrator manually assigns the survey to a different user. Survey user groups provide a way to quickly designate multiple survey users.

## Administering survey users

The list of survey users for a survey is visible on the Survey Definition and Survey Category forms. You can add or remove users from the list of survey users at any point. Note that designating a survey user does not automatically generate a survey instance for that user unless both of the following conditions are true:

-   The survey definition **Schedule** period is set to **Daily**, **Weekly**, **Monthly**, or **Yearly**. In this case the system assigns a new survey instance to each survey user at the beginning of each schedule period.
-   The user has no instances of the survey that are incomplete or that have not yet reached their expiration date.

You can designate survey users from the Survey Designer, the Survey Definition form, or the Survey Category form.

**Note:** If there are trigger conditions for a survey, do not create survey users. Instead, use the Trigger Conditions form to assign users.

-   **[Create a survey user group](../task/t_CreatingSurveyUserGroups.md)**  
Survey user groups are groups that have the **Type** field set to survey and display only the information most relevant to surveys. You can assign survey groups or any user group to surveys.
-   **[Select recipients for a survey in the Survey Designer](../task/t_SelRecipsForASurveyInDesigner.md)**  
You can assign survey users while designing or modifying the survey.
-   **[Designate a survey user](../task/t_SurveyDefinitionForm.md)**  
You can designate one survey user at a time from the Survey Definition form.
-   **[Designate or remove multiple survey users at one time](../task/t_SurveyCategoryForm.md)**  
Use the Survey Category form to designate or remove multiple survey users at a time.
-   **[Allow recipients to retake a survey](../task/t_AllowRecipientsToRetakeASurvey.md)**  
You can configure a survey to allow recipients to resubmit their answers as many times as they like, up to the survey's due date.

**Parent Topic:**[Survey administration](../reference/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports](../task/view-survey-overview.md)

[Survey designer](c_SurveyDesigner.md)

[View a survey instance](../task/t_ViewSurveyInstance.md)

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

[Surveys in Service Portal and the Now Mobile app](c_SurveyServicePortal.md)

[Surveys in ITSM Virtual Agent](survey-virtual-agent.md)

[Legacy survey migration](c_MigrateSurveys.md)

[Send survey invitations to users](../task/t_SendSurveyInvitationsToUsers.md)

[Survey trigger conditions](c_TriggerConditions.md)

[Survey categories](c_SurveyCategory.md)

[Survey definitions](c_SurveyDefinitions.md)

