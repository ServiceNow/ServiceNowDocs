---
title: Survey trigger conditions
description: Trigger conditions specify when to send a particular survey and the persons to send it to.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey trigger conditions

Trigger conditions specify when to send a particular survey and the persons to send it to.

Survey administrators can use trigger conditions to configure the system to generate a survey instance each time a specified action occurs on a specified table, for example, when an incident or change request closes. The system sends the survey to users that are related to the triggering record, for example, incident callers or change request assignees. You can choose to send a survey every time the condition is met, or you can set a probability for the system to send a survey at random when the condition is met.

Trigger conditions are ideal for sending transactional surveys. Transactional surveys generally measure satisfaction with a recent experience, such as closing an incident or purchasing an item.

**Note:** Trigger conditions are comparable to survey conditions in legacy surveys. If you migrate a legacy survey that has survey conditions, ensure that the survey conditions are deactivated before you recreate them as trigger conditions.

-   **[Configure a trigger condition for a survey](../task/t_CreateATriggerCondition.md)**  
Configure trigger conditions to specify when to send a particular survey and the persons to send it to.
-   **[Trigger condition example](../reference/r_TriggerConditionExample.md)**  
You can send out auto-triggered surveys when an incident is closed or resolved.

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

[Survey distribution](c_SurveyDistribution.md)

[Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md)

[Sentiment analysis for surveys](sentiment-analysis.md)

[Surveys in Service Portal and the Now Mobile app](c_SurveyServicePortal.md)

[Surveys in ITSM Virtual Agent](survey-virtual-agent.md)

[Legacy survey migration](c_MigrateSurveys.md)

