---
title: Producing outbound API notifications using Hermes
description: Produce an outbound notification from the ServiceNow instance using the Hermes capability. Customers can consume the details of the message from the Kafka environment in their external system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/proactive-service-exp-workflows/product-support-for-technology/hermes-stream-connect-kafka-workflow.html
release: zurich
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Handling API notifications, Use, Proactive Service Experience Workflows]
---

# Producing outbound API notifications using Hermes

Produce an outbound notification from the ServiceNow instance using the Hermes capability. Customers can consume the details of the message from the Kafka environment in their external system.

In this use case, the notifications are produced to the Hermes cluster from your ServiceNow instance. After replication from Hermes to Kafka is completed, customers can consume or pull the messages from their own Kafka.

-   To learn more about Hermes Messaging Service, see [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service.md).
-   To learn more about Apache Kafka Stream Connect, see .

In the Zurich release, the following events are supported for trouble ticket notification.

-   Create Trouble Ticket Event
-   Trouble Ticket State Change Event
-   Trouble Ticket Attribute Change Event
-   Create Trouble Ticket Event for Case

## Prerequisites

Before producing an outbound notification, the customer must create the topic in the Hermes cluster. To learn more about creating a topic in Hermes, see [Managing namespaces and topics in Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/multi-instance-framework-hermes/managing-namespaces-topics-hermes.md).

## Workflow

The workflow for producing the outbound notification by using Hermes contains the following steps:

1.  On the trigger of the trouble ticket event, the system invokes the appropriate business rule, and stamps the event type.

    To learn more about business rule that you must add to your ServiceNow instance, see [Add a business rule for a new trouble ticket event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/developer-guides/prd_evt_not-dev_gd-add_bus_rule.md).

2.  The system pushes the Glide snapshot and event type in the staging table, which acts as a queue.
3.  The producer framework picks the event and converts it to a TMF 688 complaint event payload.

    To learn more about the system properties that you must configure for the producer framework, see [Using the producer framework for outbound notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/using-producer-framework-for-trouble-ticket-notification.md).

4.  The system invokes the Producer V2 API of Stream Connect and produces the event on the Hermes Kafka topic.
5.  The Stream Connect pushes the event in the Hermes Kafka cluster.
6.  The customers can consume the message in their in-house Kafka.

**Parent Topic:**[Handling API notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/handling-trouble-ticket-notifications.md)

**Related topics**  


[EventProcessorUtilOOB - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/EventProcessorUtilOOBScopedAPI.md)

[EventQueueProcessorOOB - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/EventQueueProcessorOOBScopedAPI.md)

