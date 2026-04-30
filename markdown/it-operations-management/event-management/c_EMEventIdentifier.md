---
title: Event identifiers
description: Event fields uniquely identify each event. Event Management uses this information to determine whether to create a new alert or update an existing one.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Event identifiers

Event fields uniquely identify each event. Event Management uses this information to determine whether to create a new alert or update an existing one.

-   By default, each event is uniquely identified by the **Message Key**.
-   If the **Message Key** is not populated, the system concatenates the **Source**, **Type**, **Node**, **Resource**, and **Metric Name** fields to populate the **Message Key**.
-   If identifiers are not supplied in the event, you can add them with event rules.

**Parent Topic:**[Processing Events](processing-events.md)

