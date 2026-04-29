---
title: Create an alert for unauthorized access
description: Receive a notification when an attempt to access Hermes is received from an unauthorized IP address.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Restricting access, Configure, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an alert for unauthorized access

Receive a notification when an attempt to access Hermes is received from an unauthorized IP address.

## Before you begin

Submit a request to Customer Service and Support to enable IP address filtering in the Hermes cluster.

Configure access rules in the IP Address Access Control module. See [IP address access control](https://www.servicenow.com/docs/access?context=t_AccessControl&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Notifications**.

2.  In the Name column, search for `IP Filter Hermes`.

3.  Select the **IP Filter Hermes** notification.

4.  Activate the notification by selecting **Active**.

5.  Define one or more notification recipients.

    1.  Select the **Who will receive** tab.

    2.  Use the options to select the users or groups that need to receive the notification.


## Result

One or more selected users or groups are notified when an attempt to access Hermes is received from an unauthorized IP address.

**Parent Topic:**[Restricting access to Hermes](../concept/restricting-access-hermes-topics.md)

