---
title: Selecting queues for outbound calls
description: Agents can select a queue for their outbound calls directly from the keypad or phone directory in the Global Call window to improve routing and reporting accuracy.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-01-02"
reading_time_minutes: 1
breadcrumb: [ICC for voice calls, Integrating with contact centers, Integrate, Customer Service Management]
---

# Selecting queues for outbound calls

Agents can select a queue for their outbound calls directly from the keypad or phone directory in the Global Call window to improve routing and reporting accuracy.

## Queue selection overview

This feature provides a search interface that enables agents to find and select a queue, and then choose to either:

-   Set it as default for all outbound dialing methods
-   Apply it to the current call only

![Select a queue for outbound calls](../image/int-select-outbound-queue.png)

Agents can modify queue settings during the idle state or during active calls. The default queue selection persists until changed or log out, and applies across keypad, phone directory, and click-to-dial workflows. This feature is available for CCaaS partner integration.

## Key benefits

Queue selection for outbound calls addresses the following capabilities for contact center users:

-   Easy-to-use queue selection directly from the Global Call window.
-   Accurate reporting to track call outcomes by queue.
-   Compliance to ensure calls meet queue-specific requirements.
-   Consistent routing by applying business logic based on the selected queue.
-   Efficient workflow to reduce repetitive actions and errors.

## Queue selection Features

![Search or select a queue from the available list](../image/int-search-to-select-queue.png)

-   **Find and select a queue in Global Call**

    Search for a queue by entering in the **Search** field and select the relevant queue.

-   **Active context behavior**

    The selected queue applies to all subsequent outbound calls and remains active until the agent changes it or logs out. Only one queue is active at a time.

-   **Adjust on-demand**

    Agents can change the active queue in the idle state or during an active call. Queue changes made during a call take effect on the next outgoing call, not the current one.

-   **Consistency across dialing methods**

    The active queue persists across keypad, phone directory, and click-to-dial workflows to maintain consistent routing and reporting.

-   **UI scope**

    Queue selection is embedded within the keypad and phone directory, as required by the CCaaS platform.


See [Select queues for outbound calls from keypad, phone directory, and Interaction record](../task/select-queue-for-outbound-calls-from-keypad.md).

