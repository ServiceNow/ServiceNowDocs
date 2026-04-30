---
title: Configure email notification on application service severity change
description: Configure an email notification to notify users when there is an application service severity change.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure email notification on application service severity change

Configure an email notification to notify users when there is an application service severity change.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Configure an email notification to notify users when there is an application service severity change. The notification involves specifying when to send it, who receives it, and what it contains.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  In the **Outbound Email Configuration** section, in the **Email sending enabled** option, select **Yes** to enable sending severity information by email.

3.  Click **Save**.

4.  Navigate to **System Notification** &gt; **Email** &gt; **Notifications**.

5.  Click **New**.

    1.  In the **Email Notification Actions** form, specify these values.

        |Field|Value|
        |-----|-----|
        |Name|Type a descriptive name, for example, **Application Service severity change**.|
        |Table|Select the required service type and its corresponding table: Alert Group, Discovered Service, Technical Service, or Application service.|
        |Active|Select the check box to enable email notification.|

    2.  Click the **Who will receive** tab.

        In the **Users** area, search for and select the required user \(the user does not require System Administrator credentials\). Repeat this step for as many users that are required to receive this notification.

    3.  Click the **When to send** tab and in the **choose field** box, search for and select **Severity**.

    4.  Click the **What will it contain** tab and in the **Subject** field, type meaningful text that makes it clear to the receiver of the email notification what the content of the email is.

    5.  In the **Message HTML** message area, using the **Select variables** functions, compose the conditions under which the email notification is to be sent.

        For example, configure these variables to change severity:

        ```
        severity changed
        ```

        ```
        Severity: ${severity}
        ```

        ```
        on application service
        ```

        ```
        Name: ${name}
        ```

6.  Click **Submit**.


-   **[Configure contextual colors and icons](configure-contextual-colors-icons.md)**  
Use the **Contextual colors and icons** form to configure color, text, and icons to have different default or custom contexts, identified by a context ID.

**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

