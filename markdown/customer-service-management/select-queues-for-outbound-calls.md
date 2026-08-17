---
title: Queue selection for outbound calls
description: Queue selection for outbound calls enables agents to route calls through a specific queue directly from the Global Call window, improving routing accuracy and reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/select-queues-for-outbound-calls.html
release: australia
topic_type: concept
last_updated: "2026-01-02"
reading_time_minutes: 2
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Queue selection for outbound calls

Queue selection for outbound calls enables agents to route calls through a specific queue directly from the Global Call window, improving routing accuracy and reporting.

## Queue selection overview

A search interface enables agents to find and select a queue, and then choose to either:

-   Set it as default for all outbound dialing methods
-   Apply it to the current call only

\[Omitted image "int-select-outbound-queue.png"\] Alt text: Contact Center panel in CSM/FSM Configurable Workspace showing the Select Outbound Queue search field a dial pad

Agents can modify queue settings during the idle state or during active calls. The default queue selection persists until changed or until the agent logs out, and applies across keypad, phone directory, and click-to-dial workflows. This feature is available for CCaaS partner integration.

## Key benefits

Queue selection for outbound calls provides the following capabilities for contact center users:

-   Queue selection directly from the Global Call window.
-   Accurate reporting to track call outcomes by queue.
-   Queue-specific requirements applied to each call.
-   Consistent routing by applying business logic based on the selected queue.
-   Reduced repetitive actions and errors.

## Queue selection features

\[Omitted image "int-search-to-select-queue.png"\] Alt text: Search or select a queue from the available list

-   **Turn-on toggle for selecting queues for outbound calls**

    You can turn-on the toggle for **Select option to use queue for all outbound calls**, and set the queue as default, which applies to all outbound calls.

-   **Find and select a queue in Global Call**

    Search for a queue by entering a name in the **Search** field and select the relevant queue.

-   **Active context behavior**

    The selected queue applies to all subsequent outbound calls and remains active until the agent changes it or logs out. Only one queue is active at a time.

-   **Adjust on-demand**

    Agents can change the active queue in the idle state or during an active call. Queue changes made during a call take effect on the next outgoing call, not the current one.

-   **Consistency across dialing methods**

    The active queue persists across keypad, phone directory, and click-to-dial workflows to maintain consistent routing and reporting.

-   **UI scope**

    Queue selection is embedded within the keypad and phone directory, as required by the CCaaS platform.


See: [Using queues for outbound calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-queues-for-outbound-calls.md) and [Select queues from keypad, directory, and Interaction record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/select-queue-for-outbound-calls-from-keypad.md).

