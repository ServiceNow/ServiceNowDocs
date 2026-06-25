---
title: Survey trigger conditions
description: Trigger conditions specify when to send a particular survey and the persons to send it to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/c\_TriggerConditions.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Survey trigger conditions

Trigger conditions specify when to send a particular survey and the persons to send it to.

Survey administrators can use trigger conditions to configure the system to generate a survey instance each time a specified action occurs on a specified table, for example, when an incident or change request closes. The system sends the survey to users that are related to the triggering record, for example, incident callers or change request assignees. You can choose to send a survey every time the condition is met, or you can set a probability for the system to send a survey at random when the condition is met.

Trigger conditions are ideal for sending transactional surveys. Transactional surveys generally measure satisfaction with a recent experience, such as closing an incident or purchasing an item.

**Note:** Trigger conditions are comparable to survey conditions in legacy surveys. If you migrate a legacy survey that has survey conditions, ensure that the survey conditions are deactivated before you recreate them as trigger conditions.

-   **[Configure a trigger condition for a survey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CreateATriggerCondition.md)**  
Configure trigger conditions to specify when to send a particular survey and the persons to send it to.
-   **[Trigger condition example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_TriggerConditionExample.md)**  
You can send out auto-triggered surveys when an incident is closed or resolved.

**Parent Topic:**[Survey administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports]()

[Survey designer]()

[View a survey instance]()

[Survey users and groups]()

[Copy a survey]()

[Publish a survey]()

[Customize the appearance of a survey]()

[Survey definitions]()

[Create a survey designer template question]()

[Survey questions]()

[Survey distribution]()

[Outlook Actionable Messages]()

[Sentiment analysis for surveys]()

[Surveys in Service Portal and the Now Mobile app]()

[Surveys in ITSM Virtual Agent]()

[Legacy survey migration]()

