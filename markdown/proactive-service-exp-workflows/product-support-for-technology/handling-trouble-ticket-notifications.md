---
title: Handling API notifications
description: DOC1134021 Forward port trouble ticket name change.Use the Telecommunications API notification to inform third-party systems about the incidents or cases that are created in a reactive or proactive way in the ServiceNow instance. The customer will receive notifications regarding updates on the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/proactive-service-exp-workflows/product-support-for-technology/handling-trouble-ticket-notifications.html
release: zurich
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Proactive Service Experience Workflows]
---

# Handling API notifications

Use the Telecommunications API notification to inform third-party systems about the incidents or cases that are created in a reactive or proactive way in the ServiceNow instance. The customer will receive notifications regarding updates on the incident.

## Introduction to API notifications

Trouble ticket in the TMF ecosystem is an incident that tracks and resolves customer-reported issues, network outages, or other problems. A trouble ticket incident can be created in either the reactive or proactive way. In the reactive approach, an incident is generated after conducting root cause analysis \(RCA\) on a case that is reported due to a system fault. In the proactive approach, an incident is generated after receiving alerts, enabling for the performance of RCA or service impact analysis \(SIA\) to evaluate the impact on the services. With the trouble ticket notification feature, you can send the details of the incident to the outbound systems.

## API notification framework

The following diagram shows the components in the framework for the trouble ticket notification.

\[Omitted image "trouble-ticket-datamodel.png"\] Alt text: Trouble ticket notification data model

The trouble ticket notification uses a generic framework to send the outbound notifications to the external system. This framework supports two use cases:

1.  Publish messages to Hermes Kafka using the Hermes messaging service. The cloud customers who use the Hermes Kafka can use this architecture to receive the notification.

    To learn more, see [Producing outbound API notifications using Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/hermes-stream-connect-kafka-workflow.md).

2.  Publish messages to open message bus. This use case is message-bus agnostic and therefore supports publishing the notification to any open message bus. Both cloud and on-premise customers can use this use case. To learn more, see [Producing outbound API notifications using the open message bus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/trouble-ticket-workflow-using-pub-sub-model.md).

-   **[Producing outbound API notifications using Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/hermes-stream-connect-kafka-workflow.md)**  
Produce an outbound notification from the ServiceNow instance using the Hermes capability. Customers can consume the details of the message from the Kafka environment in their external system.
-   **[Producing outbound API notifications using the open message bus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/trouble-ticket-workflow-using-pub-sub-model.md)**  
Produce an outbound notification from the ServiceNow instance using the open message bus. Customers can consume the details of the notification from the message bus in their external system.
-   **[Using the producer framework for outbound notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/using-producer-framework-for-trouble-ticket-notification.md)**  
The producer framework picks the event from the ServiceNow instance and sends the outbound notification to the external system. You can consume the details of the notification from the messaging service that is installed in your external system.
-   **[Deactivate API notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/deactivate-trouble-ticket-notification.md)**  
Disable the business rules related to the incident and case tables to stop receiving trouble ticket notifications. Customers can disable the business rules if they don't want to leverage the trouble ticket notification capability.

**Parent Topic:**[Using Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/use-assurance-workflows.md)

