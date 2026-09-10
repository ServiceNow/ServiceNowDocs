---
title: Event forwarding
description: Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/event-forwarding-em.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Event forwarding

Accelerate the event processing testing life cycle by forwarding a stream of events from your ServiceNow production environment to your non-production environment.

Use event forwarding to forward events from one instance to another, for example, from a production to a non-production instance. Event forwarding enables you to test and evaluate event rules, event field mappings, alert management rules, and alert correlation. This testing has no impact on your production environment.

Not all monitoring sources can send events to multiple target instances. When this limitation exists, you can configure a scheduled job to periodically forward the event stream. The scheduled job forwards events from your ServiceNow instance that is connected to the monitored source to other instances.

