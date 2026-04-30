---
title: Event forwarding
description: Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event forwarding

Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.

Use event forwarding to forward events from one instance to another, for example, from a production to a non-production instance. Event forwarding enables you to test and evaluate event rules, event field mappings, alert management rules, alert correlation, and so on, without having any impact on your production environment.

Not all monitoring sources can send events to multiple target instances. In such cases, you can configure a scheduled job to periodically forward the event stream from your ServiceNow instance that is connected to the monitored source to other instances.

-   **[Set up event forwarding](../task/configure-event-forwarding-em.md)**  
Create an event forwarding configuration record to enable events to flow from one ServiceNow instance to another instance. Forwarding events to multiple target instances requires creating separate configuration records for each target instance.
-   **[Periodically run an event forwarding job](../task/configuration-management-job-em.md)**  
Schedule an event forwarding job to periodically send events to all target instances with active event forwarding configurations when the monitoring source can't send events to multiple target instances.
-   **[Create basic auth server credentials](../task/create-credentials-basic-auth.md)**  
Create credentials to access a ServiceNow instance.

**Parent Topic:**[Configuring Event Management](using-event-management.md)

