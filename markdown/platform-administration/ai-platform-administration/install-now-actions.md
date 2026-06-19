---
title: Install the Now Actions messaging app
description: As an administrator for both ServiceNow and the third-party application, find and install the Now Actions app. Install the application in ServiceNow to associate the app with your instance. Install the Now Actions messaging app from the Slack App Directory and associate the app with your instance.Associate the Now Actions messaging app with your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/install-now-actions.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Notifications in messaging applications, System notifications, Notifications, Configure core features, Administer]
---

# Install the Now Actions messaging app

As an administrator for both ServiceNow and the third-party application, find and install the Now Actions app. Install the application in ServiceNow to associate the app with your instance.

## Before you begin

To activate this feature, request the Messaging Notification plugin \(com.glide.notification.messaging\) through the HI Customer Service system. This plugin activates related plugins if they are not already active. For more information, see [Request Messaging Notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/request-messaging-notification.md).

Roles required:

-   Admin or messaging\_admin in ServiceNow
-   Administrator for Slack or Teams

**Parent Topic:**[Notifications in messaging applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/messaging-integration.md)

## Install the Now Actions messaging app for Slack

Install the Now Actions messaging app from the Slack App Directory and associate the app with your instance.

### Before you begin

Role required: admin.

### Procedure

1.  Install the Now Actions app from the Slack App Directory.

    1.  Find and install the Now Actions app in the Slack App Directory.

    2.  Click Authorize when prompted.

    3.  Enter a customized name, app description, and icon.

    4.  Configure your Now Actions web address.

        This is the base URL for your instance.

        For example, `https://<instance_name>.service-now.com/`.

    5.  Copy the JSON configuration found in the **Add your Slack credentials to your app** section for use in later steps.

2.  Associate your Slack app with your instance.

    1.  Navigate to **System Notification** → **Messaging Integration Configuration**.

    2.  Click the **Install** button next to Slack.

    3.  In the JSON Configuration pop-up, paste in the JSON configuration you copied in earlier steps.

3.  Check for installation verification.

    The Slack workspace should appear below the Slack heading on the Notification Integration page.

    \[Omitted image "slackinstalled.png"\] Alt text: Slack workspace installed

    During installation, the instance synchronizes with all public Slack channels in the workspace. New public channels added after installation will automatically synchronize with the instance. You can browse to **System Notification** &gt; **Messaging Channels** on your instance to verify that the new channel appears on the instance.


### What to do next

To update the app after installation, use the **Configure JSON Payload** and **Settings on Slack** icons on the Notification Integration page. You can view the JSON payload, view app credentials, change app appearance, or delete the app.

## Install the Now Actions messaging app for Microsoft Teams

Associate the Now Actions messaging app with your instance.

### Before you begin

Role required: admin.

### Procedure

1.  Associate your Microsoft Teams app with your instance.

    1.  Navigate to **System Notification** → **Messaging Integration Configuration**.

    2.  Click the **Install** button next to Microsoft Teams.

    3.  When a pop-up message appears to confirm redirection to Microsoft Teams to verify your identity, click **OK**.

        \[Omitted image "va-redirect-confirmation.png"\] Alt text: Redirect confirmation pop-up

    4.  When prompted, log in to Microsoft Teams with your Teams admin account.

    5.  Click Accept to accept the permissions for the app.

        \[Omitted image "va-teams-permissions.png"\] Alt text: The Now Virtual Agent app permissions screen.

    6.  If the selected workspace has already been assigned, either click **Override** to change the workspace, or click **Cancel** to leave the current assignment in place.

        After authentication, installation will start in the background. Once installation completes, a message appears confirming the installation.

        \[Omitted image "va-teams-install-success.png"\] Alt text: The successful installation message for Microsoft Teams.

    7.  Click the **app package** link to access a knowledge base article [KB0690098](https://support.servicenow.com/kb_view.do?sysparm_article=KB0690098), which contains the application package for Microsoft Teams.

    8.  Follow the steps in the article to make this package available for your Microsoft Teams users.

2.  Check for installation verification.

    During installation, the instance synchronizes with all public Teams channels. To add channels created after the install, open Microsoft Teams and @mention the app from the new channel. You can browse to **System Notification** &gt; **Messaging Channels** on your instance to verify that the new channel appears on the instance.

    The new team should appear below the Teams heading on the Notification Integration page.

    \[Omitted image "teamInstalled.png"\] Alt text: Teams workspace installed


### What to do next

To receive a ServiceNow notification in Microsoft Teams, create a message and a notification. See [Configure message content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-message-content.md) and [Create a messaging notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/create-messaging-notification.md).

