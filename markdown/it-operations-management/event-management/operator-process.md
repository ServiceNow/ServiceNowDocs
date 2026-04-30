---
title: What Event Management operators do
description: As an Event Management operator, your typical workflow involves three phases: analyzing an alert and its effect on application services, taking some type of action, and making sure the alert is finally closed.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# What Event Management operators do

As an Event Management operator, your typical workflow involves three phases: analyzing an alert and its effect on application services, taking some type of action, and making sure the alert is finally closed.

This is the last lesson in the Event Management tutorial. In this lesson, you will run through the three phases of a typical operator day-to-day workflow.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Lesson 1

</td><td align="justify">

![Overview icon](../image/progress-complete2.png)

</td><td>

[An overview of events and alerts](operator-events-alerts.md)

</td></tr><tr><td>

Lesson 2

</td><td align="justify">

![Overview of BS icon](../image/progress-complete2.png)

</td><td>

[An overview of application services](operator-application-services.md)

</td></tr><tr><td>

Lesson 3

</td><td align="justify">

![Operators icon](../image/progress-complete2.png)

</td><td>

[Event Management Service Operations Workspace](operator-user-interfaces.md)

</td></tr><tr><td>

Lesson 4

</td><td align="justify">

![Operators do icon](../image/progress-wip.png)

</td><td>

What operators do

</td></tr></tbody>
</table>Your organization will have specific policies and procedures that may differ from the phases outlined in this topic. In addition, your administrator might have customized the Event Management application so that some of these phases are automated and do not actually require any action on your part.

For the purposes of this tutorial, we will walk you through each phase and allow you to perform the tasks manually.

<table id="table_kj3_nzw_hdb"><tbody><tr><td>

Phase 1

</td><td>

Analyze and acknowledge an alert

</td><td>

In this phase, you will find an alert to work on, analyze the details, and acknowledge it so that other operators know it is a legitimate alert.

</td></tr><tr><td>

Phase 2

</td><td>

Triage an alert

</td><td>

In this phase, you take an action to help remediate the issue that caused the alert. The most common action to take is to create an incident and assign it to someone who can solve the underlying issue.

</td></tr><tr><td>

Phase 3

</td><td>

Close an alert

</td><td>

In this phase, you will verify that the alert is resolved, and then close the alert.

</td></tr></tbody>
</table>## Start here

Start out by learning how to [Analyze and acknowledge an alert](../task/operator-phase-acknowledge-analyze.md).

-   **[Operator phase 1: Analyze and acknowledge an alert](../task/operator-phase-acknowledge-analyze.md)**  
As an Event Management operator, the first thing you should do is access alerts and then find the ones you want to focus on. You can open the Alert form to analyze the details, and then acknowledge it to let other operators know that the issue causing the alert should be addressed in some way.
-   **[Operator phase 2: Triage an alert](../task/operator-phase-triage-incident.md)**  
After you analyze and acknowledge an alert, you must triage it. The triage phase involves verifying alert correlation and taking an action to help resolve the issue that caused the alert. This topic covers the most common triage task: creating an incident from an alert.
-   **[Operator phase 3: Close an alert](../task/operator-close-alert.md)**  
After you take action on an alert, you can verify several items on the alert and then close it.

**Parent Topic:**[Event Management Operator Tutorial](operator-guide-em.md)

