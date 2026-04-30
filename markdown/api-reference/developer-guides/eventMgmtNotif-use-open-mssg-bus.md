---
title: Create outbound Order Management notifications using the open message bus
description: Learn how to produce an outbound notification from a ServiceNow instance using the open message bus. Customers can consume the details of the notification from the message bus in their external system.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Create outbound Order Management notifications using the open message bus

Learn how to produce an outbound notification from a ServiceNow® instance using the open message bus. Customers can consume the details of the notification from the message bus in their external system.

## Introduction to outbound order management notifications

In this event-driven architecture, notifications are produced to the open message bus from your ServiceNow® instance. The framework contains topic synchronization and topic picker mechanisms. The topic synchronization mechanism synchronizes the topics that you have created in the instance containing the open message bus. When the event occurs in the framework, the topic picker mechanism picks the relevant topic and publishes the message to the topic using a REST proxy. Customers can consume the outbound notification from the message bus in their external system.

## Supported Order Management events

The following events are supported for Order management notification.

Product Order Management:

1.  CancelProductOrderCreateEvent
2.  CancelProductOrderStateChangeEvent
3.  ProductOrderCreateEvent
4.  ProductOrderDeleteEvent
5.  ProductOrderJeoperdyAlertEvent
6.  ProductOrderStateChangeEvent

Service Order Management:

1.  CancelServiceOrderCreateEvent
2.  CancelServiceOrderStateChangeEvent
3.  ServiceOrderCreateEvent
4.  ServiceOrderDeleteEvent
5.  ServiceOrderJeoperdyAlertEvent
6.  ServiceOrderStateChangeEvent

## Prerequisites

Before producing outbound notifications, it’s necessary to create the egress topics in the Topic \[sn\_api\_notif\_mgmt\_topic\] table in the ServiceNow® instance. When you create an egress topic, the system runs a business rule and attempts to synchronize the topic to the message bus based on configuration. To learn more about manually creating a topic in the Topic table, see [Create a topic](https://www.servicenow.com/docs/access?context=create-topic-API-notification&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US). The system synchronizes only the egress topic with the message bus in the external system. The `user_created` field in the associated topic record is set to `true`.

Alternatively, you can create the topics on the message bus in your external system and push them into the Topic table in ServiceNow® instance. To do this, invoke the [Event Management Topic Open API](../../../inbound-rest/concept/event_management_topic-api.md#) endpoint, which stores the topic in the Topic \[sn\_api\_notif\_mgmt\_topic\] table of the instance. The user\_created field in the associated topic record is set to false.

