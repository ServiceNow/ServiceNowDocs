---
title: Link your ServiceNow user account to your Slack or MS Teams account for Now Actions
description: Link your ServiceNow account to your Slack or Teams account to take action on ServiceNow notifications from within Slack or Teams. If you do not link accounts, you can still receive notifications within group channels. However, you cannot to approve ServiceNow requests or take action on notifications from within Slack or Teams.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Notifications in messaging applications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Link your ServiceNow user account to your Slack or MS Teams account for Now Actions

Link your ServiceNow account to your Slack or Teams account to take action on ServiceNow notifications from within Slack or Teams. If you do not link accounts, you can still receive notifications within group channels. However, you cannot to approve ServiceNow requests or take action on notifications from within Slack or Teams.

## Before you begin

Role required: none

## Procedure

1.  Open the Slack or Teams application

2.  Navigate to the Now Actions bot, which can be found in the left panel of Slack under Apps, and in the left panel of Teams in the **Chat** tab.

3.  Start a conversation with the Now Actions bot.

    The bot then presents a link to authenticate.

    ![An authentication message displayed in Teams.](../../virtual-agent/images/va-teamsauthprompt.png "Authentication message")

4.  Click the **Connect to ServiceNow** link.

    A new browser tab opens and prompts the user to Deny or Confirm the connect between your Slack or Teams account and your ServiceNow account. This link will expire five minutes after it is displayed.

5.  Click **Confirm** to link the accounts.

    ![A confirmation prompt to allow a link between ServiceNow and Slack or Teams](../../virtual-agent/images/va-link-confirm-prompt.png)

6.  After confirmation, you are directed to the instance user record.

    A confirmation message is displayed at the top of the screen.

    ![The link confirmation message shown on the user record.](../../virtual-agent/images/va-link-confirm-success.png)


**Parent Topic:**[Notifications in messaging applications](../concept/messaging-integration.md)

