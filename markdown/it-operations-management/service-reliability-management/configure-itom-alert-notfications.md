---
title: Configure when to send alert notifications for ITOM Mobile
description: Keep your teams informed by configuring when ITOM Mobile Agent sends a notification about an alert.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring ITOM Mobile Agent, ITOM Mobile Agent, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Configure when to send alert notifications for ITOM Mobile

Keep your teams informed by configuring when ITOM Mobile Agent sends a notification about an alert.

## Before you begin

Role required: admin

## About this task

By default, ITOM Mobile Agent sends a push notification and email when an alert meets these conditions:

-   **Assigned to is empty** - The alert isn't assigned to anyone.
-   **State is not Closed** - The alert state isn't closed. It's either empty, flapping, open, or reopen.
-   **Severity is Critical** - The alert severity is critical. It isn't clear, empty, OK, major, minor, or warning.

You can update those conditions as needed. For example, the ITOM Mobile Agent app can send notifications for both critical and major alerts. However, if you customize the conditions, the conditions don't receive future release updates. That behavior is intentional to avoid overwriting your work.

**Note:** To get push notifications, you must log in to ITOM Mobile Agent. If you log out, you only get email notifications.

This procedure is for admins configuring alert push notifications and emails. To manage other notification features, see [Customizing other mobile settings for ITOM Mobile Agent](../reference/itom-mobile-other-customizations.md).

## Procedure

1.  Navigate to **All** &gt; **Mobile App Builder**.

2.  Search for and select **ITOM Mobile Agent**.

3.  Select **Mobile notifications**.

4.  In the **When to send** section, update or add to the assigned to, state, and severity conditions.

    For example, adding the condition **OR \[Severity\]\[is\]\[Major\]** under the condition **\[Severity\]\[is\]\[Critical\]** sends a push notification and email when the **Severity** field of an alert is Critical or Major.

5.  Implement your changes by selecting **Save**.

    The page displays `Your changes have been saved`.


## What to do next

To customize who receives emails about alerts, see [Customize ITOM Mobile Agent email recipients](customize-itom-email-recipients.md). You can also customize other notification features, such as setting custom notification tones and overriding the Do Not Disturb setting for critical issues. See [Customizing other mobile settings for ITOM Mobile Agent](../reference/itom-mobile-other-customizations.md) for more information.

