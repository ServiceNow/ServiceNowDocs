---
title: Handling API notifications
description: Use the Telecommunications API notification to inform third-party systems about the incidents or cases that are created in a reactive or proactive way in the ServiceNow instance. The customer will receive notifications regarding updates on the incident.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Product Support for Technology]
---

# Handling API notifications

Use the Telecommunications API notification to inform third-party systems about the incidents or cases that are created in a reactive or proactive way in the ServiceNow instance. The customer will receive notifications regarding updates on the incident.

## Introduction to API notifications

Trouble ticket in the TMF ecosystem is an incident that tracks and resolves customer-reported issues, network outages, or other problems. A trouble ticket incident can be created in either the reactive or proactive way. In the reactive approach, an incident is generated after conducting root cause analysis \(RCA\) on a case that is reported due to a system fault. In the proactive approach, an incident is generated after receiving alerts, enabling for the performance of RCA or service impact analysis \(SIA\) to evaluate the impact on the services. With the trouble ticket notification feature, you can send the details of the incident to the outbound systems.

## API notification framework

The following diagram shows the components in the framework for the trouble ticket notification.

![Trouble ticket notification data model](../image/trouble-ticket-datamodel.png "Trouble ticket notification data model")

The trouble ticket notification uses a generic framework to send the outbound notifications to the external system. This framework supports two use cases:

1.  Publish messages to Hermes Kafka using the Hermes messaging service. The cloud customers who use the Hermes Kafka can use this architecture to receive the notification.

    To learn more, see [Producing outbound API notifications using Hermes](hermes-stream-connect-kafka-workflow.md).

2.  Publish messages to open message bus. This use case is message-bus agnostic and therefore supports publishing the notification to any open message bus. Both cloud and on-premise customers can use this use case. To learn more, see [Producing outbound trouble ticket notifications using the open message bus](trouble-ticket-workflow-using-pub-sub-model.md).

