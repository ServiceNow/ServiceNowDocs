---
title: Create default content in a provider
description: Create and use the default content for a notification that doesn't have a content provider or some of the fields in the content provider aren’t present.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create provider notification, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create default content in a provider

Create and use the default content for a notification that doesn't have a content provider or some of the fields in the content provider aren’t present.

## Before you begin

Role required: admin

## Procedure

1.  Enter sys\_notification\_content.list in the application navigator.

    A list of **Notification Contents** shows up.

2.  Select **New Provider Content**.

    1.  Select and hold any column header and then select **Configure** &gt; **List Control**.

    2.  Clear the **Omit new button** to display the **New Provider Content** field.

    **Note:** Both shared content and provider content can be default content. Provider content has been considered for this example.

3.  Select the type of Notification Content that you would like to create.

4.  Fill the **Notification Content** form for the type you have selected in the previous step.

    **Note:** The **is default** field is visible only if the **Notifications** field is not present.

5.  Select **Submit**.

    A new default content has been created.


**Parent Topic:**[Create provider notification](../concept/create-provider-notification-using.md)

