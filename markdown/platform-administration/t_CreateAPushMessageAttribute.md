---
title: Create a push message attribute definition
description: Push message attribute definitions allow you to create reusable properties for push message content specification.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup using custom push app, Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Create a push message attribute definition

Push message attribute definitions allow you to create reusable properties for push message content specification.

## Before you begin

1.  [Activate push notifications](t_ActivatePushNotifications.md)
2.  \(iOS only\) [Upload a push certificate to your instance](upload-push-cert.md)
3.  [Create a push application record for your custom app](t_CreateAMobileApplication.md)
4.  [Create push message content](t_CreateAMobileMessageLayout.md)

Role required: admin or push\_admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at [Mobile push notifications](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=zurich&pubname=zurich-mobile&ft:locale=en-US)

## About this task

Use an attribute definition to specify a default push action script or string that you can then use in the push message content.

You can override these attributes by creating any [push message attribute values](t_CreateAPushMessageAttributeValue.md).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Message Content**.

2.  Select a content record or script record.

3.  In the Push Message Attribute Definitions related list, click **New**.

4.  Fill out the fields on the form \(see table\).

5.  Click **Submit**.

<table id="table_wdd_2rs_ks"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attribute Name

</td><td>

Enter a descriptive name for the layout.

</td></tr><tr><td>

Attribute Type

</td><td>

Select the type of attribute:-   **Action**: An action to take on the instance, as defined by a script.
-   **String**: An arbitrary string to send as part of the message content. The string can specify items like a button label in the message.


</td></tr><tr><td>

Default Script

</td><td>

Select the mobile action script that tells the instance what to do when it receives a response from the push notification. This option appears if you select **Action** for the **Type**.

</td></tr><tr><td>

Default Value

</td><td>

Specify an arbitrary string value to be placed in the attribute that is used by the message content. For example, the string could specify a button label. This option appears if you select **String** for the **Type**.

</td></tr></tbody>
</table>
## What to do next

If you want to override default attribute definitions, see [Create an attribute value or action for a push message](t_CreateAPushMessageAttributeValue.md).

