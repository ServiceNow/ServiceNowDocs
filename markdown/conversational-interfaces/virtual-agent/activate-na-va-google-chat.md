---
title: Activate Now Assist in Virtual Agent for Google Chat
description: Add Now Assist in Virtual Agent to your Google Chat bot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/activate-na-va-google-chat.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
keywords: [Now, Assist, Microsoft, Teams, Virtual, Agent, Integration, MS, MSTeams]
breadcrumb: [Install Conversational Integration with Google Chat, Conversational Integration with Google Chat, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Activate Now Assist in Virtual Agent for Google Chat

Add Now Assist in Virtual Agent to your Google Chat bot.

## Before you begin

Role required: admin or virtual\_agent\_admin

Create a self-configured bot for Google Chat. For more information, see [Integrate Virtual Agent with Google Chat using the self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/installing-ci-google-chat.md).

**Note:** Ensure you've updated the version of your Google Chat app in the **Version** field.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Under **Now Assist in Virtual Agent \(default\)**, select the **Edit** button.

3.  Under the **Settings** tab, select **Display experiences**, then select **Channels**.

4.  Choose the self-configured bot for the Teams channel experience you want to activate by selecting the **Select row** check box next to its name.

5.  Select **Save and continue**.

6.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

7.  Under Integrations, in the Google Chat tile, select **Manage**.

8.  In the Self-configured tile, next to your bot's name, select the **Manage bot** icon \(\[Omitted image "three-dots-icon.png"\]\), and then select **Manage bot** from the drop-down menu.

9.  Select **Edit configuration**, and then select the check box next to **Google chat**.

10. Select **Save**.

    The bot is now active for Google Chat, and the bot's Configuration tab opens.

11. Select **Download** to save the manifest zip file.


## What to do next

Upload the manifest to Google Chat to make your bot experience available in the Microsoft global apps store, which will also activate the Custom Engine Agent \(CEA\) in Google Chat. For more information, see [Upload the manifest package file to publish your bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/upload-package-file-msteams.md).

**Parent Topic:**[Install Conversational Integration with Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/install-ci-google-chat.md)

