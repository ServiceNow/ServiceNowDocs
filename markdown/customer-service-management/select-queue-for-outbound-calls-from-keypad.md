---
title: Select queues for outbound calls from keypad, phone directory, and Interaction record
description: This procedure describes how to select a queue and place outbound calls using the Global Call keypad and phone directory in the CCaaS platform. It covers both standard and mandatory queue selection scenarios.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-01-02"
reading_time_minutes: 1
breadcrumb: [Selecting queues for outbound calls, ICC for voice calls, Integrating with contact centers, Integrate, Customer Service Management]
---

# Select queues for outbound calls from keypad, phone directory, and Interaction record

This procedure describes how to select a queue and place outbound calls using the Global Call keypad and phone directory in the CCaaS platform. It covers both standard and mandatory queue selection scenarios.

## Before you begin

Role required: Agent managing voice calls

-   Log in to the CCaaS platform with the required permissions.
-   Confirm access to the Global Call component in your workspace.
-   Ensure the Interaction Controls Component \(ICC\) component is enabled.
-   Verify assignment to at least one queue or skill group.

Follow these steps to select a queue and place an outbound call using the keypad, phone directory, or an Interaction record.

## Procedure

1.  Navigate to your configured CSM Configurable Workspace and select the phone icon to launch the call keypad.

    The **Select outbound queue** field displays giving you the option to either search for a queue by name or select one from the list of available queues.

    You can also click-to-dial from an Interaction record. In the keypad, select and set a queue as default for outbound calls. Once you set a queue for outbound calls and click-to-dial from a different Interaction record, the Active Call window displays. This window is integrated with the ICC, instead of the Global Call window.

    ![Click-to-call from an Interaction record](../image/int-click-to-call-with-queue-selection.png)

2.  In the **Search** field, begin entering the name of the queue to search for it or select the queue directly from the list displaying available queues.

3.  The selected queue displays in the search field, confirming your choice.

4.  If you set a queue as default, it applies to all your outbound calls.

    ![Enable the toggle to set a queue to default for all outbound calls](../image/int-set-queue-to-default.png)

5.  Use the keypad or the phone directory to enter or select the phone number.

    The dial button becomes enabled when a valid number is entered in the keypad.

6.  Select the dial button to initiate the outbound call with the selected queue and the interface transitions to an active call state displaying call details.

7.  After the call ends, complete any required wrap up activities, such as selecting a wrap-up code and adding notes, and select **Submit &amp; close**.


## What to do next

The queue you selected remains active for your next outbound call. You can change the queue at any time by repeating steps 2 and 3, or you can continue using the same queue for subsequent calls.

