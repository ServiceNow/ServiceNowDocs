---
title: ITSM Virtual Agent pre-built actionable notifications
description: Send interactive messages to an employee through Virtual Agent, based on pending tasks or alerts. Deflect some of the most common ITSM incidents to ITSM Virtual Agent, reduce incident volume to Service Desk, and help employees discover ITSM Virtual Agent as a resolution channel.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ITSM Virtual Agent, IT Service Management]
---

# ITSM Virtual Agent pre-built actionable notifications

Send interactive messages to an employee through Virtual Agent, based on pending tasks or alerts. Deflect some of the most common ITSM incidents to ITSM Virtual Agent, reduce incident volume to Service Desk, and help employees discover ITSM Virtual Agent as a resolution channel.

## Actionable notifications

Actionable notifications are interactive messages that Virtual Agent sends to the end user when the user takes certain actions on non-conversational service channels. These notifications have buttons that enable the recipient to perform certain actions, such as adding a comment or requesting a live agent. When you create an actionable notification, you associate an action with a published Virtual Agent topic, a scriptable action, or a flow action that handles the action to be performed. For example, Virtual Agent can send a notification when an employee submits an incident through email or the ServiceNow® Service Portal, if there are any updates or actions needed from the employee. Employees can resolve the incident directly in the Virtual Agent conversation, without involving a live agent.

Admin or Virtual Agent admin \(virtual\_agent\_admin\) users activate notifications and the ITSM Virtual Agent Conversation topics.

To create your own custom notifications, see [Configuring Virtual Agent notifications](https://www.servicenow.com/docs/access?context=configuring-va-notifications&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Pre-built ITSM actionable notifications

The following pre-built notifications are available for ITSM Virtual Agent. You must activate these notifications in Workflow Studio before you can use them. For details, see [Set up actionable notifications for ITSM Virtual Agent](../task/setup-actionable-notifications.md).

|I want to|Pre-built notifications|
|---------|-----------------------|
|Notify users of changes to their incidents|[Actionable notifications for incidents in ITSM Virtual Agent](../reference/itsm-actionable-notification-flows.md)|
|Notify users of changes to their Service Catalog requests|[Actionable notifications for Service Catalog requests in ITSM Virtual Agent](../reference/va-itsm-notifications-service-catalog.md)|
|Notify users of approvals for change requests or KB articles|[Actionable notifications for approvals in ITSM Virtual Agent](../reference/va-itsm-notifications-approvals.md)|
|Notify users when their password is about to expire|[Actionable notifications for Password Reset for Virtual Agent](../reference/itsm-va-notifications-password-reset.md)|
|Notify users of changes to virtual machines|[Actionable notifications for virtual machines in ITSM Virtual Agent](../reference/itsm-va-notifications-virtual-machine.md)|
|Notify users when Virtual Agent finds a topic that can resolve the end user's issue|[Actionable notifications for Issue Auto Resolution in ITSM Virtual Agent](../reference/itsm-va-notifications-iar.md)|

-   **[Actionable notifications for incidents in ITSM Virtual Agent](../reference/itsm-actionable-notification-flows.md)**  
Notify employees of pending tasks and incident alerts with notifications from ITSM Virtual Agent.
-   **[Actionable notifications for Service Catalog requests in ITSM Virtual Agent](../reference/va-itsm-notifications-service-catalog.md)**  
Notify employees of Service Catalog tasks and alerts with notifications from ITSM Virtual Agent.
-   **[Actionable notifications for approvals in ITSM Virtual Agent](../reference/va-itsm-notifications-approvals.md)**  
Notify employees of approvals for requests with notifications from ITSM Virtual Agent.
-   **[Actionable notifications for Password Reset for Virtual Agent](../reference/itsm-va-notifications-password-reset.md)**  
Use Virtual Agent to notify employees when their password is about to expire.
-   **[Actionable notifications for virtual machines in ITSM Virtual Agent](../reference/itsm-va-notifications-virtual-machine.md)**  
Notify users when a change is made to a virtual machine \(VM\) instance.
-   **[Actionable notifications for Issue Auto Resolution in ITSM Virtual Agent](../reference/itsm-va-notifications-iar.md)**  
Notify employees when Virtual Agent finds a topic that matches the end user's intent.
-   **[Issue Auto Resolution for ITSM Virtual Agent](itsm-va-auto-resolution.md)**  
Proactively deflect common ITSM incidents to ITSM Virtual Agent. Initiate a conversation with an end user after they submit an incident through a non-conversational service channel, if an existing ITSM Virtual Agent conversation can resolve the issue.
-   **[Tracking deflections in ITSM Virtual Agent](itsm-va-deflection.md)**  
You can use the pre-built deflection topics and topic blocks in Virtual Agent conversations to track the incidents that ITSM Virtual Agent helped to resolve.

**Parent Topic:**[ITSM Virtual Agent](itsm-virtual-agent.md)

**Related topics**  


[Issue Auto Resolution for ITSM Virtual Agent](itsm-va-auto-resolution.md)

