---
title: Surveys in ITSM Virtual Agent
description: You can use surveys in ITSM Virtual Agent to collect survey responses from users through conversational questionnaires \(pre-chat and post-chat surveys\) in the chat client.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Surveys in ITSM Virtual Agent

You can use surveys in ITSM Virtual Agent to collect survey responses from users through conversational questionnaires \(pre-chat and post-chat surveys\) in the chat client.

A chat survey is available in ITSM Virtual Agent through the Provide Virtual Agent Feedback topic. The logic that renders the survey dynamically is called from the re-usable Survey topic block. It is common to use the Provide Virtual Agent Feedback topic as the survey setup topic in the general definitions of ITSM Virtual Agent, so that users automatically receive a survey at the end of their conversations. For information about the Survey topic block, see ITSM Virtual Agent.

When you select the **Chat Survey** check box for a survey, the following conditions are validated for surveys on ITSM Virtual Agent.

-   Survey should contain only one metric category.
-   Survey can contain only these metric types.
    -   Attachment
    -   Boolean
    -   Check box
    -   Choice
    -   Date
    -   Date/Time
    -   Image scale
    -   Number
    -   Numeric scale
    -   Percentage
    -   Scale
    -   String

For information on configuring a survey, see [Modify a survey definition](../task/t_ModifySurveyDefinitions.md) and [Configure a survey in the survey designer](../task/t_ConfigSurveyInSurveyDesgnr.md).

The following capabilities are supported for the survey:

-   Dependent survey fields
-   Introduction and end notes

## Association between a survey and Virtual Agent chat

After a survey is submitted in a Virtual Agent conversation, a survey instance is created. This instance displays the following information:

-   Trigger ID, which is the sys\_id of the associated interaction ID created in the Virtual Agent chat
-   Trigger table, which is the interaction table

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

[Surveys in Service Portal and the Now Mobile app](c_SurveyServicePortal.md)

[Legacy survey migration](c_MigrateSurveys.md)

[bundle-itsm.itsm-virtual-agent]

