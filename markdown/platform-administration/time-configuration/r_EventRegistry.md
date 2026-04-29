---
title: Event registry
description: You can use events to schedule actions or tasks to occur when conditions are fulfilled.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event scheduling, System scheduler, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Event registry

You can use events to schedule actions or tasks to occur when conditions are fulfilled.

For example:

-   **kb.view**

    An event triggered when a user views a Knowledge Base article. You use it to trigger the script action Knowledge View that create a Knowledge Use record every time an article is viewed.

-   **incident.commented**

    An event triggered when a user comments on an article, used by two incidents commented email notifications.

-   **Inactivity Monitors**

    If a record has not been updated for a defined length of time, an inactivity monitor triggers an event.

-   **Script Actions**

    Scripts that trigger when an event is recorded in the log. You can set scripts to execute whenever a particular activity occurs in the platform, rather than at a particular time, such as scheduled jobs, or in response to particular conditions, such as [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US).

-   **Notifications**

    You can also use events to trigger Email Notifications when an event is recorded in the log.


**Parent Topic:**[Event scheduling](../../time/concept/c_ScheduleEvents.md)

**Related topics**  


[Set an inactivity monitor](../../time/task/t_SetAnInactivityMonitor.md)

