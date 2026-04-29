---
title: Event forwarding
description: Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event forwarding

Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.

Use event forwarding to forward events from one instance to another, for example, from a production to a non-production instance. Event forwarding enables you to test and evaluate event rules, event field mappings, alert management rules, alert correlation, and so on, without having any impact on your production environment.

Not all monitoring sources can send events to multiple target instances. In such cases, you can configure a scheduled job to periodically forward the event stream from your ServiceNow instance that is connected to the monitored source to other instances.

