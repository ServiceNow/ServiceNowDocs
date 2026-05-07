---
title: Producing outbound API notifications using Hermes
description: Produce an outbound notification from the ServiceNow instance using the Hermes capability. Customers can consume the details of the message from the Kafka environment in their external system.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Handling API notifications, Use, Product Support for Technology]
---

# Producing outbound API notifications using Hermes

Produce an outbound notification from the ServiceNow instance using the Hermes capability. Customers can consume the details of the message from the Kafka environment in their external system.

In this use case, the notifications are produced to the Hermes cluster from your ServiceNow instance. After replication from Hermes to Kafka is completed, customers can consume or pull the messages from their own Kafka.

-   To learn more about Hermes Messaging Service, see [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   To learn more about Apache Kafka Stream Connect, see [Using Stream Connect for Apache Kafka](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

In the Australia release, the following events are supported for trouble ticket notification.

-   Create Trouble Ticket Event
-   Trouble Ticket State Change Event
-   Trouble Ticket Attribute Change Event
-   Create Trouble Ticket Event for Case

## Prerequisites

Before producing an outbound notification, the customer must create the topic in the Hermes cluster. To learn more about creating a topic in Hermes, see [Managing namespaces and topics in Hermes](https://www.servicenow.com/docs/access?context=managing-namespaces-topics-hermes&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Workflow

The workflow for producing the outbound notification by using Hermes contains the following steps:

1.  On the trigger of the trouble ticket event, the system invokes the appropriate business rule, and stamps the event type.

    To learn more about business rule that you must add to your ServiceNow instance, see [Add a business rule for a new trouble ticket event](https://www.servicenow.com/docs/access?context=prd_evt_not-dev_gd-add_bus_rule&version=australia&pubname=australia-api-reference&ft:locale=en-US).

2.  The system pushes the Glide snapshot and event type in the staging table, which acts as a queue.
3.  The producer framework picks the event and converts it to a TMF 688 complaint event payload.

    To learn more about the system properties that you must configure for the producer framework, see [Using the producer framework for outbound notifications](using-producer-framework-for-trouble-ticket-notification.md).

4.  The system invokes the Producer V2 API of Stream Connect and produces the event on the Hermes Kafka topic.
5.  The Stream Connect pushes the event in the Hermes Kafka cluster.
6.  The customers can consume the message in their in-house Kafka.

**Related topics**  


[EventProcessorUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=EventProcessorUtilOOBScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[EventQueueProcessorOOB - Scoped](https://www.servicenow.com/docs/access?context=EventQueueProcessorOOBScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

