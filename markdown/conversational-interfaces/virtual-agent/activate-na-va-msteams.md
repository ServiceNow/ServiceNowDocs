---
title: Activate ServiceNow Otto for Virtual Agent for Microsoft Teams
description: Add ServiceNow Otto for Virtual Agent to your Microsoft Teams and Microsoft Copilot bot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/activate-na-va-msteams.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
keywords: [Otto, Microsoft, Teams, Virtual, Agent, Integration, MS, MSTeams]
breadcrumb: [Install, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Activate ServiceNow Otto for Virtual Agent for Microsoft Teams

Add ServiceNow Otto for Virtual Agent to your Microsoft Teams and Microsoft Copilot bot.

## Before you begin

Role required: admin or virtual\_agent\_admin

Create a self-configured bot for Microsoft Copilot. For more information, see [Setting up the Self-configured bot for using Microsoft Copilot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/setup-self-bot-copilot.md).

**Note:** Ensure you've updated the version of your Microsoft Teams app in the **Version** field.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Assistants** tab.

3.  On the **SeviceNow Otto for Virtual Agent \(default\)** tile, select **Edit**.

4.  Select **Review display experiences**.

5.  Select the **Channels** tab.

6.  Choose the self-configured bot for the Teams channel experience you want to activate by selecting the **Select row** check box next to its name.

7.  Select **Save and continue**.

8.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.

9.  Under Integrations, in the Microsoft Teams tile, select **Manage**.

10. In the Self-configured tile, next to your bot's name, select the **Manage bot** icon \(\[Omitted image "three-dots-icon.png"\]\), and then select **Manage bot** from the drop-down menu.

11. Select **Edit configuration**, and then select the check box next to **Copilot**.

    **Note:** The **Copilot** option will be a **Message extension** option instead if you haven't selected the matching bot in Step 4.

12. Select **Save**.

    The bot is now active for Copilot, and the bot's Configuration tab opens.

13. Select **Download** to save the manifest zip file.


## What to do next

Upload the manifest to Microsoft Teams to make your bot experience available in the Microsoft global apps store, which will also activate the Custom Engine Agent \(CEA\) in Microsoft Copilot. For more information, see [Upload the manifest package file to publish your bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/upload-package-file-msteams.md).

**Parent Topic:**[Install Conversational Integration with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/teams-install.md)

