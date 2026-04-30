---
title: Schedule periods
description: The available schedule periods are Only Once, No Limit, Daily, Weekly, Monthly, and Yearly.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Survey definitions, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Schedule periods

The available schedule periods are **Only Once**, **No Limit**, **Daily**, **Weekly**, **Monthly**, and **Yearly**.

The default schedule period is **No Limit**. When you set the schedule period to anything except **Only Once** or **No Limit**, the system creates a corresponding scheduled job. The scheduled job performs the following actions.

-   Ensures that a user can take one survey instance of the same survey per schedule period.
-   Generates a new survey instance for each survey user at the beginning of the new schedule period, as long as the survey user does not have an incomplete instance of that survey. A survey instance is incomplete if the state is not **Complete**.

For example, if you set the schedule period to **Monthly** and someone attempts to [send survey invitations](../task/t_SendSurveyInvitationsToUsers.md) twice in the same day, the system generates survey instances for the survey users the first time only. At the beginning of the next schedule period, the system generates another survey instance for each survey user who completed the previous one.

Schedule periods are enforced by the **Expiration date** field on the survey instance. As long as the survey instance expiration date has not passed, the assigned user cannot receive a new survey instance. When the system generates a survey instance and the schedule period is anything except **No Limit**, the **Expiration date** field is automatically set to the appropriate date. For example, if the schedule period is **Weekly**, the expiration date is a week after the survey instance is generated.

If you change the schedule period, the scheduled job updates automatically to the correct schedule. However, users who have survey instances for the survey cannot receive new survey instances until their existing survey instances expire, regardless of the new schedule period.

Consider the following example: Sal Pindell receives a survey instance when the schedule period is **Weekly**. The next day, a survey administrator changes the schedule period to **No Limit**. Sal cannot receive another survey instance until one of the following actions occurs.

-   Seven days pass from the time Sal's survey instance was generated.
-   A survey administrator deletes Sal's survey instance.

After one of these actions occurs, Sal can receive a new survey instance anytime, as long as he has no incomplete instances of the survey.

**Note:** If you use a trigger condition for a survey, ensure the schedule period is set to **No Limit**. Trigger conditions use a different method to regulate how often users can receive survey instances.

**Related topics**  


[Publish a survey](../task/t_PublishASurvey.md)

[Survey trigger conditions](c_TriggerConditions.md)

