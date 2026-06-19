---
title: Implement the overflow menu for active calls
description: Configure the toolbar layout order for the active call component so that call control buttons exceeding the available toolbar slots appear in the overflow menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/implement-overflow-menu-icc.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 2
keywords: [overflow menu, active call component, toolbar layout order, ICC, call controls]
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Implement the overflow menu for active calls

Configure the toolbar layout order for the active call component so that call control buttons exceeding the available toolbar slots appear in the overflow menu.

## Before you begin

Identify the list of call control buttons to enable and their intended display order.

Role required: contact center admin

## About this task

The toolbar on the active call component displays a maximum of six call control buttons. When recording is enabled, the recording button anchors in the first position, reducing the available slots to five. When the number of enabled buttons exceeds the available slots, the system renders the remaining buttons in the overflow menu. If all enabled buttons fit within the toolbar slots, no overflow button appears.

**Note:** The overflow menu appears only on the active call component within the interaction record. It does not appear in the global call component.

\[Omitted image "active-call-component-overflow-menu.png"\] Alt text: Overflow menu on the active call component showing call control buttons.

## Procedure

1.  In UI Builder, open the active call component for your workspace.

2.  Locate the **toolbarLayoutOrder** client state parameter and set the button order using the values in the following table.

    The default button order in **toolbarLayoutOrder** matches the table. You can update the order in UI Builder.

    |Button label|**toolbarLayoutOrder** value|
    |------------|----------------------------|
    |Mute|`mute`|
    |Hold|`hold`|
    |Keypad|`dtmf`|
    |Transfer|`transfer`|
    |Agent Initiated Wrap-Up|`wrapUpInitiated`|
    |Supervisor Help Request|`help_request`|
    |Report Quality Issue|`flag`|

    **Note:** If your implementation includes recording, the recording button is first and cannot be repositioned. Adjust **toolbarLayoutOrder** and the button order in UI Builder together to keep them in sync.

    Two buttons have specific conditions:

    -   **Supervisor Help Request** is always available from the overflow menu but is inactive when a request is active. Agents can request supervisor assistance but must end or cancel it from the modal at the top of the active call component participant section.
    -   **Open Wrap-Up** appears only when enabled. Agents use it to complete post-call wrap-up tasks.
3.  In UI Builder, set the button order to match the sequence defined in **toolbarLayoutOrder**.

    Keeping both settings in sync prevents the recording button from being repositioned.

4.  Select **Save**.

5.  Confirm the overflow menu behavior by initiating a test call.

    Buttons exceeding the toolbar slot limit appear in the overflow menu on the active call component.

    **Note:** Buttons in the overflow menu behave similarly to their toolbar counterparts, for example, Mute, Hold, Report Quality Issue, and Open Wrap-Up each disable briefly after being selected.

    The overflow menu icon appears on the active call component toolbar.


## Result

The active call component toolbar is configured. Call control buttons that exceed the available slots are accessible from the overflow menu within the interaction record.

