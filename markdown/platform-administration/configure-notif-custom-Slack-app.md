---
title: Set up notifications for a custom Slack app
description: Send ServiceNow notifications to users via your own Slack bot.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Notifications in messaging applications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up notifications for a custom Slack app

Send ServiceNow notifications to users via your own Slack bot.

## Before you begin

-   Request Integration Hub
-   [Request the Messaging Notification plugin](request-messaging-notification.md)
-   Create a custom application for Slack

Role required: admin or messaging\_admin

## Procedure

1.  Create a JSON for your custom Slack application.

    Ensure that your JSON matches the following example format:

    ```
    {
    "bot_user_id" : "U9TLFR6TA",
    "scope" : "bot,channels:read",
    "client_id" : "294380102274.335446283495",
    "client_secret" : "ed0da5fe1f844fdac15a9e1ac1b0b831",
    "verification_token" : "YXSNsRhioCeU8h9Fm2k4ACuO",
    "app_id" : "A9VD48BEK",
    "access_token" : "xoxp-294380102274-295238228534-335452648487-2fac31f923dadd7ff30f2bc8c852809d",
    "bot_access_token" : "xoxp-333695856928-6pNwnO3Y6vNSGI7KCAIPwv6V",
    "team_id" : "T8NB63082",
    "team_name" : "sn-notif-ext-test",
    "user_id" : "U8P706QFQ",
    "bot_username": "empdmyers1snnotifext"
    }
    ```

    To get the Bot User ID, copy the member ID of the bot user in the Slack app.

    The Scope is always `bot,channels:read`.

    To get the Client ID, Client Secret, and Verification Token, see the Basic Information page in your Slack workspace.

    To get the App ID, copy the 9-character identifier from the app URL in your Slack workspace.

    To get the Access Token and Bot Access Token, see the OAuth &amp; Permissions page in your Slack workspace.

    To get the Team ID, view the HTML source code for your Slack workspace page.

    The Team Name is the same as your subdomain in your Slack workspace.

    To get the User ID, copy the member ID for your own account in the Slack app.

    The Bot Username is the name that you assigned to the bot user in Slack.

2.  In your ServiceNow instance, navigate to **System Notification** &gt; **Messaging** &gt; **Messaging Integration Configuration**.

3.  Next to the Slack listing, click **Install**.

4.  On the JSON Configuration window, paste the JSON that you created in Step [1](configure-notif-custom-Slack-app.md#create-json).

    ![Example JSON](../image/custom-slack-app-json.png)

5.  Click **Submit**.

6.  On the confirmation window, click **Skip**.

    ![Confirmation window](../image/slack-confirmation-window.png)


## Result

The system creates a notification channel for your custom Slack app automatically.

## What to do next

-   Link ServiceNow user accounts to your custom Slack app so that users can take action on notifications that are delivered by your Slack bot.
-   For each user account that you link, enable the notification channel using the system settings.
-   Create notifications for your custom Slack app by following the steps in [Create a messaging notification](create-messaging-notification.md) and [Configure message content](configure-message-content.md).

**Parent Topic:**[Notifications in messaging applications](../concept/messaging-integration.md)

**Related topics**  


[Slack API documentation](https://api.slack.com/)

