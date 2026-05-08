---
title: Configuring Telecommunications API notifications
description: Configure the Telecommunications API notification in the ServiceNow instance.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Service Operations Management]
---

# Configuring Telecommunications API notifications

Configure the Telecommunications API notification in the ServiceNow instance.

## Modeling the Telecommunications API notification workflow

The following steps help to configure the Telecommunications API notification in the ServiceNow instance.

1.  [Create a topic](../task/create-topic-API-notification.md): You can create topics either by manually typing the external message details or automatically collecting the available topics from the external system.
2.  [Create a topic subscription](../task/create-subscription-api-notification.md): You subscribe to the available topics for incoming notifications from the external system, based on the customer preference. Additionally, you generate the callback URL and register the subscription.
3.  [Activate the endpoint of the Telecommunications Alarm Management Open API connection](../task/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md): To receive responses from the external system, activate the subscribed endpoints of the Telecommunications Alarm Management Open API connection in the Workflow Studio.
4.  Provide the callback URL to the external system for receiving notifications. Customer can also reuse the callback URL. When requests from TMF 688 hit the Callback URL, it initiates the Default Alarm Event Notification Trigger flow to create an event.

    To learn more about the functions to handle Event Notification Management Open API requests that are triggered by external trigger definitions to create, update, and delete events, see Event Notification Management Open API and TMFTopicEventAPIUtilOOB - Scoped.


This workflow creates an event in the Event Management application. To learn more about using Event Management, see Event Management.

**Related topics**  


[System components installed with Telecommunications API notifications](../reference/alarm-management-user-roles.md)

[External event management via Telecommunications API notifications](telecommunications-api-notification.md)

