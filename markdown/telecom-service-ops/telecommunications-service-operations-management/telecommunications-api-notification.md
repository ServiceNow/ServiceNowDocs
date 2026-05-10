---
title: External event management via Telecommunications API notifications
description: Use the Telecommunications API notification to receive the external events that occurring in the customer network system so that you can promptly respond to them in the ServiceNow.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Service Operations Management]
---

# External event management via Telecommunications API notifications

Use the Telecommunications API notification to receive the external events that occurring in the customer network system so that you can promptly respond to them in the ServiceNow.

## Introduction to Telecommunications API notification

Telecommunications API notification is a feature available in the Telecommunications Alarm Management Open API application. The Telecommunications API notification enables ServiceNow to receive the incoming notifications that occurring in the external network system and responds to them in a timely manner. It enables the broadcasting of events to the external systems through platform capabilities by eliminating the need for point connections.

Telecommunications API notification receives incoming notifications from the external systems that are subscribed on your network. When the notifications are received from the external system, you can create the events for the responses by using the Event Management application. Based on the collected information, the Event Management provides dashboards showing a consolidated view of all service-impact events.

## Telecommunications API notification data model

The Telecommunications API notification enables ServiceNow to receive incoming notifications through the event-driven architectures such as the Publisher/Subscriber \(Pub/Sub\) subscription model, Hermes, and Kafka Stream Connect. While cloud customers have the flexibility to select between both architectures, on-premise customers are limited to using their own Kafka or Pub/Sub subscription model.

-   To learn more about Stream connect for Apache Kafka Stream, see [Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/stream-connect-apache-kafka.md).
-   To learn more about Hermes Messaging Service, see [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service.md).

In the Pub/Sub model, incoming notifications are categorized into topics. You use ServiceNow to publish the incoming notifications to these topics, and subscribers \(customers\) have the flexibility to select the topics to which they want to subscribe. This process enables subscribers to select only those messages that align with their interests. For example, if there are 10 topics for incoming messages from the external system, a customer can opt to subscribe to two of them based on their requirement. Consequently, when notifications are received from the external system, events are generated specifically for the two topics to which the customer has subscribed.

**Related topics**  


[Configuring Telecommunications API notifications](configuring-telecommunications-api-notifications.md)

[System components installed with Telecommunications API notifications](../reference/alarm-management-user-roles.md)

