---
title: Set up the Slack account
description: Set up the Slack account.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Sidebar and Slack, Sidebar and Slack, Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Set up the Slack account

Set up the Slack account.

## Before you begin

Role required: none

## Procedure

1.  From the Slack [developer program](https://api.slack.com/developer-program), sign in to your Slack developer account.

2.  On the Slack dashboard, select **Your apps** from the upper right-hand corner of the screen.

3.  From the Your Apps screen, select **Create an App.**

4.  On the Create an app dialog, select **From scratch**.

5.  On the Name app &amp; choose workspace dialog, fill out the fields:

    -   App Name - name for the application you are going to create. Make a note of the app name because you will need it in the remaining procedures.
    -   Pick a workspace to develop your app in - from the drop-down list, select the workspace where your app will reside. Make a note of the app name because you will need it in the remaining procedures.
6.  Select **Create App**.

7.  In a browser window, enter `https://api.slack.com/apps` and select the app you created in step 5.

8.  From settings, select **Oauth &amp; Permissions**.

9.  In the Redirect URLs dialog, enter `https://{instance_url}/oauth_redirect.do`

10. Select **Add New Direct URL**.

11. Add these Oauth scopes from the User Token Scope section:

    |OAuth Scope|Description|
    |-----------|-----------|
    |channels:history|View messages and other content in a user's public channels.|
    |channels:read|View basic information about public channels in a workspace.|
    |channels:write|Manage a user's public channels and create new ones on a user's behalf.|
    |channels:write.invites|Invite members to public channels.|
    |chat:write|Send messages on a user's behalf.|
    |files:write|Upload, edit, and delete files on a user's behalf.|
    |groups:read|View basic information about a user's private channels.|
    |groups:write|Manage a user's private channels and create new ones on a user's behalf.|
    |groups:write.invites|Invite members to private channels.|
    |im:read|View basic information about a user's direct messages.|
    |im:write|Start direct messages with people on a user's behalf.|
    |mpin:read|View basic information about a user's group direct messages.|
    |mpin:write|Start group direct messages with people on a user's behalf.|
    |users:read|View people in a workspace.|
    |users:read.email|View email addresses of people in a workspace.|

12. Add these Oauth scopes from the Bot Token Scope section:

    |OAuth Scope|Description|
    |-----------|-----------|
    |users:read|View people in a workspace.|
    |users:read.email|View email addresses of people in a workspace.|


