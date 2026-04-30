---
title: Event identifiers
description: Event identifiers uniquely distinguish one event from another. Event Management uses these identifiers to determine whether to create a new alert or update an existing one.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event identifiers

Event identifiers uniquely distinguish one event from another. Event Management uses these identifiers to determine whether to create a new alert or update an existing one.

By default, an event is uniquely identified by the following fields:

-   **Message Key**
-   **Domain**
-   **Category**

Changing the **Category** field \(for example, through a Background Script or Business Rule\) may lead to unexpected system behavior.

If the **Message Key** is not provided, the system automatically generates one by concatenating the following fields:

-   **Source**
-   **Type**
-   **Node**
-   **Resource**
-   **Metric Name**

If the above fields are not defined in the incoming event, you can define them using event rules.

