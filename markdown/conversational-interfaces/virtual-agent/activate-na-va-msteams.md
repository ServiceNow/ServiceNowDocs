---
title: Activate Now Assist in Virtual Agent for Microsoft Teams
description: Add Now Assist in Virtual Agent to your Microsoft Teams and Microsoft Copilot bot.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now, Assist, Microsoft, Teams, Virtual, Agent, Integration, MS, MSTeams]
breadcrumb: [Install, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Activate Now Assist in Virtual Agent for Microsoft Teams

Add Now Assist in Virtual Agent to your Microsoft Teams and Microsoft Copilot bot.

## Before you begin

Role required: admin or virtual\_agent\_admin

Create a self-configured bot for Microsoft Copilot. For more information, see [Setting up the Self-configured bot for using Microsoft Copilot](../concept/setup-self-bot-copilot.md).

**Note:** Ensure you've updated the version of your Microsoft Teams app in the **Version** field.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

2.  Select **Now Assist in Virtual Agent \(default\)**.

3.  Under the **Display experience** tab, select **Channels**.

4.  Choose the self-configured bot for the Teams channel experience you want to activate by selecting the **Select row** check box next to its name.

5.  Select **Save and continue**.

6.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

7.  Under Integrations, in the Microsoft Teams tile, select **Manage**.

8.  In the Self-configured tile, next to your bot's name, select the **Manage bot** icon \(![](../images/three-dots-icon.png)\), and then select **Manage bot** from the drop-down menu.

9.  Select **Edit configuration**, and then select the check box next to **Copilot**.

    **Note:** The **Copilot** option will be a **Message extension** option instead if you haven't selected the matching bot in Step 4.

10. Select **Save**.

    The bot is now active for Copilot, and the bot's Configuration tab opens.

11. Select **Download** to save the manifest zip file.


## What to do next

Upload the manifest to Microsoft Teams to make your bot experience available in the Microsoft global apps store, which will also activate the Custom Engine Agent \(CEA\) in Microsoft Copilot. For more information, see [Upload the manifest package file to publish your bot](upload-package-file-msteams.md).

**Parent Topic:**[Install Conversational Integration with Microsoft Teams](teams-install.md)

