---
title: Handling the external events using Telecommunications API notification
description: Use the Telecommunications API notification to receive the external events that occurring in the customer network system so that you can promptly respond to them in the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Telecommunications Service Operations Management]
---

# Handling the external events using Telecommunications API notification

Use the Telecommunications API notification to receive the external events that occurring in the customer network system so that you can promptly respond to them in the ServiceNow AI Platform.

## Overview

Telecommunications API notification is a feature available in the Telecommunications Alarm Management Open API application. The Telecommunications API notification enables ServiceNow to receive the incoming notifications that occurring in the external network system and responds to them in a timely manner. It enables the broadcasting of events to the external systems through platform capabilities by eliminating the need for point to point connections.

Telecommunications API notification receives incoming notifications from the external systems that are subscribed on your network. When the notifications are received from the external system, you can create the events for the responses by using the Event Management application. Based on the collected information, the Event Management provides dashboards showing a consolidated view of all service-impact events.

## Telecommunications API notification data model

The following diagram shows the components in the data model for the Telecommunications API notification.

![Infographic showing the components in the Telecommunications API notification data model. For the description, see the following texts.](../images/telcomm-api-notification-data-model.png "API notification data model")

The Telecommunications API notification enables ServiceNow to receive incoming notifications through the event-driven architectures such as the Publisher/Subscriber \(Pub/Sub\) subscription model, Hermes, and Kafka Stream Connect. While cloud customers have the flexibility to select between both architectures, on-premise customers are limited to using their own Kafka or Pub/Sub subscription model.

-   To learn more about Stream connect for Apache Kafka Stream, see [Using Stream Connect for Apache Kafka](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   To learn more about Hermes Messaging Service, see [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

In the Pub/Sub model, incoming notifications are categorized into topics. You use ServiceNow to publish the incoming notifications to these topics, and subscribers \(customers\) have the flexibility to select the topics to which they want to subscribe. This process enables subscribers to select only those messages that align with their interests. For example, if there are 10 topics for incoming messages from the external system, a customer can opt to subscribe to two of them based on their requirement. Consequently, when notifications are received from the external system, events are generated specifically for the two topics to which the customer has subscribed.

## Modeling the Telecommunications API notification workflow

The following steps help to configure the Telecommunications API notification in the ServiceNow instance.

1.  [Create a topic](../task/create-topic-API-notification.md): You can create topics either by manually typing the external message details or automatically collecting the available topics from the external system.
2.  [Create a topic subscription](../task/create-subscription-api-notification.md): You subscribe to the available topics for incoming notifications from the external system, based on the customer preference. Additionally, you generate the callback URL and register the subscription.
3.  [Activate the endpoint of the Telecommunications Alarm Management Open API connection](../task/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md): To receive responses from the external system, activate the subscribed endpoints of the Telecommunications Alarm Management Open API connection in the Workflow Studio.
4.  Provide the callback URL to the external system for receiving notifications. Customer can also reuse the callback URL. When requests from TMF 688 hit the Callback URL, it initiates the Default Alarm Event Notification Trigger flow to create an event.

    To learn more about the functions to handle Event Notification Management Open API requests that are triggered by external trigger definitions to create, update, and delete events, see [Event Notification Management Open API](https://www.servicenow.com/docs/access?context=event_open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) and [TMFTopicEventAPIUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=tmftopiceventapiutiloobScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


This workflow creates an event in the Event Management application. To learn more about using Event Management, see [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

-   **[Create a topic](../task/create-topic-API-notification.md)**  
Create a topic and publish the incoming notifications from the external system to the topic. By creating the topics, subscribers can select the topics to which they want to subscribe.
-   **[Create a topic subscription](../task/create-subscription-api-notification.md)**  
Subscribe to the topic in the ServiceNow AI Platform that you want respond to the incoming notification from the external system. By subscribing to the topic, the subscriber receives the notifications based on the topics that you subscribe to.
-   **[Activate the endpoint of the Telecommunications Alarm Management Open API connection](../task/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md)**  
Activate the endpoint of the Telecommunications Alarm Management Open API connection. By activating the endpoint, you receive the incoming notifications from the external system for the topic that you registered.
-   **[Telecommunications API notification user roles](../reference/alarm-management-user-roles.md)**  
Administrators can assign user roles to grant access to the API notification database tables. The following standard roles for the Topic \[sn\_api\_notif\_mgmt\_topic\] and Topic Subscription \[sn\_api\_notif\_mgmt\_subscription\] tables are included in the ServiceNow system.

**Parent Topic:**[Telecommunications Service Operations Management](telecom-service-operations-mgt-overview.md)

