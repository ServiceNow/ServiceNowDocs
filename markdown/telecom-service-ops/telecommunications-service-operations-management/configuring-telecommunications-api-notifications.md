---
title: Configuring Telecommunications API notifications
description: Configure the Telecommunications API notification in the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configuring-telecommunications-api-notifications.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configuring Telecommunications API notifications

Configure the Telecommunications API notification in the ServiceNow instance.

## Modeling the Telecommunications API notification workflow

The following steps help to configure the Telecommunications API notification in the ServiceNow instance.

1.  [Create a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-topic-API-notification.md): You can create topics either by manually typing the external message details or automatically collecting the available topics from the external system.
2.  [Create a topic subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-subscription-api-notification.md): You subscribe to the available topics for incoming notifications from the external system, based on the customer preference. Additionally, you generate the callback URL and register the subscription.
3.  [Activate the Telecommunications Alarm Management Open API endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md): To receive responses from the external system, activate the subscribed endpoints of the Telecommunications Alarm Management Open API connection in the Workflow Studio.
4.  Provide the callback URL to the external system for receiving notifications. Customer can also reuse the callback URL. When requests from TMF 688 hit the Callback URL, it initiates the Default Alarm Event Notification Trigger flow to create an event.

    To learn more about the functions to handle Event Notification Management Open API requests that are triggered by external trigger definitions to create, update, and delete events, see [Event Notification Management Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/event_open-api.md) and [TMFTopicEventAPIUtilOOB - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/tmftopiceventapiutiloobScopedAPI.md).


This workflow creates an event in the Event Management application. To learn more about using Event Management, see [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_EM.md).

-   **[Create a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-topic-API-notification.md)**  
Create a topic and publish the incoming notifications from the external system to the topic. By creating the topics, subscribers can select the topics to which they want to subscribe.
-   **[Create a topic subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-subscription-api-notification.md)**  
Subscribe to the topic in the ServiceNow AI Platform that you want respond to the incoming notification from the external system. By subscribing to the topic, the subscriber receives the notifications based on the topics that you subscribe to.
-   **[Activate the Telecommunications Alarm Management Open API endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md)**  
Activate the endpoint of the Telecommunications Alarm Management Open API connection. By activating the endpoint, you receive the incoming notifications from the external system for the topic that you registered.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[System components installed with Telecommunications API notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/alarm-management-user-roles.md)

[External event management via Telecommunications API notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/telecommunications-api-notification.md)

