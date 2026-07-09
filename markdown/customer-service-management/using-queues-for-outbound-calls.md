---
title: Using queues for outbound calls
description: Use the toggle in the Global Call window to set a default queue for all your outbound calls during your current browser session, or select a queue for every call.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/using-queues-for-outbound-calls.html
release: australia
topic_type: concept
last_updated: "2026-01-02"
reading_time_minutes: 1
breadcrumb: [Queue selection, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Using queues for outbound calls

Use the toggle in the Global Call window to set a default queue for all your outbound calls during your current browser session, or select a queue for every call.

## Turn on or Turn off toggle for selecting queues for outbound calls

The toggle enables you to set a default queue for all your outbound calls during your current browser session. This removes the need to select a queue for every outbound call. The the toggle is disabled when the selected outbound queue field is empty.

\[Omitted image "int-select-outbound-queue.png"\] Alt text: Contact Center panel in CSM/FSM Configurable Workspace showing the Select Outbound Queue search field on the dial pad

-   **When you Turn on or Turn off the toggle, your selection is saved in your browser for the current session**
    -   Your toggle setting persists across all browser tabs while you remain logged in.
    -   After you close and reopen a tab, your toggle setting remains unchanged.
    -   Your setting is cleared when you close the browser.
-   **When you Turn on the toggle and select a default queue for all outbound calls**
    -   The selected queue is applied to all outbound calls you make during the session.
    -   The call window or dialog does not reappear when you make subsequent outbound calls.
    -   After turning on the toggle and selecting a queue, you can close the queue selection window.
    -   Regardless of how you initiate an outbound call, the call uses the selected queue.
-   **When you Turn off the toggle, and have not set a default queue for all outbound calls**
    -   Every time you make an outbound call, the call window displays.
    -   For every outbound call, you can select a new outbound queue or modify the previously configured one.
    -   With the toggle is turned off, a selected outbound queue can be used for that call only.
    -   After closing the window, the selection window appears again on the next call attempt.

See [Select queues from keypad, directory, and Interaction record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/select-queue-for-outbound-calls-from-keypad.md).

