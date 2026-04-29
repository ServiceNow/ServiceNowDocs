---
title: Advanced tasks for the Event Management operator
description: As an Event Management operator, you might need to perform additional tasks that are outside of your typical workflow, or tasks that you need to perform only once.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Advanced tasks for the Event Management operator

As an Event Management operator, you might need to perform additional tasks that are outside of your typical workflow, or tasks that you need to perform only once.

|Advanced task|Description|
|-------------|-----------|
|[Customize your alert list view](../task/operator-create-dashbaord-view.md)|Get to the alerts you need to analyze as soon as possible.|
|[Work with flapping alerts](../task/operator-handle-alerts-flapping.md)|If an alert is in the flapping state, it means that the underlying issue keep reoccurring. You should triage the alert again and look for another solution.|
|[Handle alerts while CIs are in maintenance](../task/operator-alerts-CIs-in-maintenance.md)|Learn how to handle alerts on a CI that is in the maintenance state, which means it is undergoing some type of change.|
|[Adjust alert impact while triaging an alert](../task/operator-adjust-impact-rules.md)|You can change impact rules, which affects how alert impact is calculated and alert severity.|

-   **[Customize your alert list view](../task/operator-create-dashbaord-view.md)**  
You can create one or more customized alert list views that show only the information pertinent to you. For example, you might want to focus only on the alerts for application services in a specific location, or only the alerts for application services of high criticality.
-   **[Work with flapping alerts](../task/operator-handle-alerts-flapping.md)**  
If an alert is in the flapping state, you might need to triage the alert again.
-   **[Handle alerts while CIs are in maintenance](../task/operator-alerts-CIs-in-maintenance.md)**  
When an alert occurs on a CI that is in the maintenance state, the alert state is also changed to maintenance. You should find and monitor the states of these alerts. Later, when changes on the CI are complete, finish triaging the alert and close it.
-   **[Adjust alert impact while triaging an alert](../task/operator-adjust-impact-rules.md)**  
As an Event Management operator, you might need to modify the impact that an alert has on an application service and on the CIs in a service. Do this when you think that the impact does not accurately represent what you see in your network environment so other operators and administrators see the correct impact information.

**Parent Topic:**[Event Management Operator Tutorial](operator-guide-em.md)

