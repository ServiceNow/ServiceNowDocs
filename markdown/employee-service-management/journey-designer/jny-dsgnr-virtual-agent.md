---
title: Integrating HR Service Delivery Virtual Agent Conversations app with Journey designer
description: Install the HR Service Delivery Virtual Agent Conversations app to enable Journey designer to send actionable notifications as nudges to employees and managers on configured communications channels.
locale: en-US
release: yokohama
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrations for Journey designer app, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Integrating HR Service Delivery Virtual Agent Conversations app with Journey designer

Install the HR Service Delivery Virtual Agent Conversations app to enable Journey designer to send actionable notifications as nudges to employees and managers on configured communications channels.

The HR Service Delivery Virtual Agent Conversations app displays action buttons to enable interactions and complete the actions. Using HR Service Delivery Virtual Agent Conversations app aids faster approvals and task completion by engaging employees and managers on the channels that they are at.

## Activation information

Install the latest version of [HR Service Delivery Virtual Agent Conversations \[sn\_hr\_va\]](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8c5545573d8130000e588e54cf6a71a) to enable actionable notification in Journey designer.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Integrating the Learning Posts app with Journey designer enables you to manage recommended learning for journeys from inside Journey designer.

## Predefined Virtual Agent notifications for HR Service Delivery

The HR Service Delivery Virtual Agent Conversations app provides predefined notifications to help your employees, mentors, and managers receive information about the common tasks in HR Service Delivery.

Notifications are sent to employees, managers, and mentors that are associated with a journey. The following HR Service Delivery Virtual Agent notifications are available:

-   New Journey created – Notify Employee
-   New Journey created – Notify Manager
-   New Journey created – Notify Mentor
-   New Mentor\(s\) added – Notify Manager
-   New Mentor\(s\) added – Notify Employee
-   New Mentor\(s\) added – Notify Mentor​
-   Journey Tasks Overdue​
-   Journey JA task Commented​
-   Journey LE task Approval Requested​

**Note:** For a holistic experience of the journey outcome in Virtual Agent, turn on all the six Journey created scenario notifications \(Manager, Mentor, and Employee\).

For more information about HR Service Delivery Virtual Agent Conversations and topic blocks, see [Virtual Agent for HR Service Delivery](hr-virtual-agent-conversations.md#).

## Actionable notification in the Journey designer app

Journey designer use case: When notifications are configured, a notification is sent when a new journey is created and published. The employee is notified of it on the configured CI channel. The manager is prompted to add a mentor. After the mentor is added, notifications are sent to the employee and the mentor.

## Virtual Agent Designer

As and admin, go to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**. Filter on the following:

-   **Type** = `Topics`
-   **Category** = `HRSD Actionable Notifications`
-   **Status** = `Active`

There are four action topics linked to Journey designer provided in the base system of the application.

-   \_add\_comment\_to\_ja\_task - Add a comment. These comments are alsi displayed in the journey task activity.
-   \_add\_mentor\_to\_journey - Add a mentor. You can select a mentor from the list provided by the Virtual agent or search a person by typing the name.
-   \_approve\_le\_approval\_activity - Approve the request assigned as a part of the journey.
-   \_reject\_le\_approval\_activity - Reject the request assigned as a part of the journey.

You can also associate other actions with the notifications. For more information, see [Add actions to the notification content](https://www.servicenow.com/docs/access?context=noti-select-provider-actions-order&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Parent Topic:**[Integrations for Journey designer app](jny-integrations-1.md)

