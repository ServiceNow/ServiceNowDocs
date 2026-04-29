---
title: Exploring system events
description: Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response.
locale: en-US
release: australia
product: System Events
classification: system-events
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [System Events, Build workflows]
---

# Exploring system events

Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response.

## System events overview

Learn about how system events function as triggers for actions and enable process automation.

Realize the benefits of leveraging system events by doing the following tasks in your instance:

-   Create events
-   Log events
-   Implement automated job scheduling
-   Move an event
-   Register events
-   Reprocess events
-   Pass event parameters from a work-flow to a notification

## System events users

|User|Description|
|----|-----------|
|Administrator|Administrators leverage system events to trigger automated actions and work-flows based on specific occurrences in the platform, enabling asynchronous processing and responsive automation. They can generate events via scripts or business rules, register them in the Event Registry, and handle them using notifications, script actions, or flows.|
|Business analysts|Business analysts analyze trends and processes by leveraging events to capture specific system activities, generate logs, or send data to analytic tools for better decision-making and process improvement.|
|Compliance officers|Compliance officers help to ensure adherence to regulatory requirements by using events to log critical activities, generate compliance reports, or initiate corrective actions when deviations from standards are detected.|
|Customer support|Customer support employees use system events to enhance customer service by triggering automated responses to customer requests, creating follow-up tasks, or escalating unresolved cases to appropriate teams.|
|Developers|Developers create and manage system events to integrate modules, trigger work-flows, and implement custom logic in response to user actions or record changes, helping to ensure extensibility and dynamic system behavior.|
|HR administrators|HR professionals use system events to automate HR processes, such as notifying employees of updates, generating on-boarding work-flows when a new hire is recorded, or triggering document reviews during off-boarding.|
|ITOM/ITSM|IT service managers use system events to monitor and automate ITSM processes, such as sending notifications for SLA breaches, escalating incidents, or triggering task work-flows, helping to ensure efficient IT service delivery and compliance with SLAs.|
|Marketing teams|Marketing teams automate customer engagement by using events to trigger campaign actions, such as sending promotional emails or updating CRM systems when specific conditions \(e.g., customer interaction\) are met.|
|Operations teams|Operations teams monitor and respond to operational alerts or system changes by triggering events that initiate corrective actions, such as restarting services, updating CMDB records, or notifying relevant teams of maintenance schedules.|
|Project managers|Project managers use system events to trigger notifications for project updates, create task dependencies automatically, or update stakeholders when milestones are achieved, enabling better project tracking and communication.|
|Security analysts|Security analysts leverage system events to trigger immediate responses to security incidents, such as creating alerts, generating logs, or initiating containment work-flows in response to detected threats or vulnerabilities.|

## System events benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Allows users to define new events that can be triggered by specific conditions or actions, enabling customized work-flows and automated responses.|[Create an event](../task/t_CreateYourOwnEvent.md)|Developers, Administrators, IT Service Managers|
|Captures event activity in logs for auditing, debugging, and monitoring system behavior, providing insights into event performance and bottlenecks.|[Event logs](../reference/r_EventLogs.md)|Administrators, Compliance Officers, Security Analysts|
|Schedules jobs to be executed automatically at specific times or intervals, ensuring routine tasks are performed without manual intervention.|[Implement automated job scheduling](../task/auto-job-scheduling.md)|Operations Teams, IT Service Managers, Administrators|
|Transfers events between queues or categories, helping optimize processing priority and load balancing in event-driven systems.|[Move an event](../task/move_event.md)|Administrators, Developers|
|Registers custom or system-defined events in the platform to make them available for triggering specific actions or work-flows.|[Register an event](../task/t_RegisterAnEvent.md)|Developers, Administrators|
|Provides the ability to reprocess failed or incomplete events, ensuring system reliability and minimizing the impact of errors.|[Reprocess an event](../task/t_ReprocessAnEvent.md)|IT Operations Teams, Developers, Administrators|
|Enables seamless transfer of contextual data from work-flows to notifications, ensuring messages contain relevant and actionable information for recipients.|[Pass event parameters from a work-flow to a notification](../../notification/task/t_PassEventParameters.md)|Developers, IT Service Managers, HR Professionals|

## What to explore next

To learn more about configuring and using System events, see:

-   [Configuring system events](configuring-system-events.md)
-   [Managing system events](managing-system-events.md)
-   [System events reference](../reference/system-events-reference.md)

-   **[System Events](events.md)**  
Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response to the conditions.
-   **[Event registry](c_EventRegistry.md)**  
The events registry lists the events the system recognizes. Use registered events to automate other activities, such as script actions or notifications.

**Parent Topic:**[System Events](system-events-landing.md)

