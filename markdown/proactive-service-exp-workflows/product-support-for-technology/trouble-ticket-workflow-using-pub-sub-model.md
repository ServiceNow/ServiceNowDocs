---
title: Producing outbound trouble ticket notifications using the open message bus
description: Produce an outbound notification from the ServiceNow instance using the open message bus. Customers can consume the details of the notification from the message bus in their external system.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Handling API notifications, Use, Product Support for Technology]
---

# Producing outbound trouble ticket notifications using the open message bus

Produce an outbound notification from the ServiceNow instance using the open message bus. Customers can consume the details of the notification from the message bus in their external system.

In this event-driven architecture, the notifications are produced to the open message bus from your ServiceNow instance. The framework contains topic synchronization and topic picker mechanisms. The topic synchronization mechanism synchronizes the topics that you have created in the ServiceNow instance with the open message bus. When the event occurs in the framework, the topic picker mechanism picks the relevant topic and publishes the message to the topic using a REST proxy. Customers can consume the outbound notification from the message bus in their external system.

In the Australia release, the following events are supported for trouble ticket notification.

-   Create Trouble Ticket Event
-   Trouble Ticket State Change Event
-   Trouble Ticket Attribute Change Event
-   Create Trouble Ticket Event for Case

## Prerequisites

Before producing outbound notifications, it’s necessary to create the egress topics on the Topic \[sn\_api\_notif\_mgmt\_topic\] table in the ServiceNow instance. When you create an egress topic, the system runs a business rule and attempts to synchronize the topic to the message bus based on configuration. To learn more about manually creating a topic in the Topic table, see Create a topic. The system synchronizes only the egress topic with the message bus in the external system. The **user\_created** field in the associated topic record is set to true.

Alternatively, you can create the topics on the message bus in your external system and push them into the Topic table in ServiceNow instance. The customers invoke the Event Management Topic Open API endpoint, which stores the topic in the Topic \[sn\_api\_notif\_mgmt\_topic\] table of ServiceNow instance. The **user\_created** field in the associated topic record is set to false. To learn more about the methods that are used when processing the Event Management Topic Open API endpoint, see Event Management Topic Open API.

## Workflow

The workflow for producing the outbound notification by using the open message bus contains the following steps:

1.  On the trigger of the trouble ticket event, the system invokes the appropriate business rule, and stamps the event type.

    To learn more about the business rule that you must add to your ServiceNow instance, see Add a business rule for a new trouble ticket event.

2.  The system pushes the Glide snapshot and event type in the staging table, which acts as a queue.
3.  The producer framework picks the event and converts it to a TMF 688 complaint event payload.

    To learn more about the producer framework, see [Using the producer framework for outbound notifications](using-producer-framework-for-trouble-ticket-notification.md).

4.  The topic picker mechanism determines the topics, which are compatible with the event type. Topic picker performs the following steps to check the compatibility of the topics:

    1.  The System scans the topics that have the **Type** field set as **Egress** in the topic table.
    2.  The system checks the header query and content query of all egress topics and matches the compatibility with the event payload.
    To learn more details about how to customize the existing topic picker mechanism, see OpenMessageBusEventPublisherOOB - Scoped.

5.  The system sends the list of compatible topics and event payload to the spoke selector.
6.  The spoke selector, which the customer has configured, invokes the REST step that is configured for each topic and sends to the message bus REST Proxy in the external system.

    To learn more about the method for sending messages to the spoke selector, see OpenMessageBusEventPublisherOOB - Scoped and Configure the Producer Event Notification Framework to use the Open Message Bus.

7.  The customers can consume the message in their message bus REST Proxy.

**Related topics**  


[bundle-crapiref.EventProcessorUtilOOBScopedAPI]

[bundle-crapiref.EventQueueProcessorOOBScopedAPI]

[bundle-tsom.telecommunications-api-notification]

