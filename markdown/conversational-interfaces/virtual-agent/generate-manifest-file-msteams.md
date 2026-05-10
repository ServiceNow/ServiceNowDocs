---
title: Auto-generate the manifest file for uploading on Microsoft Teams
description: Auto-generate the manifest file and customize the branding of your Microsoft Teams app so that you can make Virtual Agent available in your organization.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Auto-generate, manifest, file, uploading, Microsoft, Teams, MSTeams, Virtual Agent, self-configured bot]
breadcrumb: [Integrate VA with MS Teams using self-configured bot, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Auto-generate the manifest file for uploading on Microsoft Teams

Auto-generate the manifest file and customize the branding of your Microsoft Teams app so that you can make Virtual Agent available in your organization.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

An automated manifest file generator on the new Microsoft Teams UI automatically fills in the bot ID and updates the other settings \(such as branding\) based on input from you, the administrator​. The manifest file generator also enables a one-select download of the manifest package.

-   Before you generate a manifest file, you must create a self-configured bot \(or ensure that one has already been created\) in the ServiceNow instance. You can then generate a manifest package for each self-configured bot that you create​.
-   After you save the manifest form, you can download the manifest zip package, which contains the following three files:

    -   manifest.json
    -   color.png
    -   outline.png
    You can edit the manifest form and redownload it as many times as you want.​


**Note:** This feature is only applicable when you’re setting up the Virtual Agent integration with Microsoft Teams. If you intend to use ServiceNow for Microsoft Teams with ITSM or HR capabilities, select the **Learn more** link next to **Planning to enable additional ITSM and HR integrations** on the Bot Configuration page. That way, you can configure the manifest in a separate module instead of continuing to configure the manifest here. For more information, see [Create and download the manifest file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/download-manifest-file-mt.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings**, in the Channels and routing section, select **View All**.

3.  On the Channels and integrations page, in the Microsoft Teams tile, select **Manage**.

4.  In the Self-configured bot section, select the **Manage Bot** icon ![Manage Bot icon.](../images/manage-bot-icon.png).

    If you haven't enabled Message Extension and you are accessing it for the first time, you see a Turn on new feature alert message that informs you that the Message Extension feature for your Microsoft Teams integration is now available to be turned on.

5.  On the **Configuration** tab, select **Edit configuration** and on the form, fill in the fields.

<table id="table_jvq_fkj_z5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Name

</td><td>

Short display name for your app.**Note:** Ensure that the name doesn’t exceed 30 characters.

</td></tr><tr><td>

Full Name

</td><td>

Full name of your app. Use the full name if the short name of the app exceeds 30 characters.**Note:** Ensure that the full name doesn’t exceed 100 characters.

</td></tr><tr><td>

Bot \(Client\) ID

</td><td>

Unique Microsoft generated identifier.This field is automatically tied to the bot creation step and can't be altered.

</td></tr><tr><td>

Short description

</td><td>

Short description of your app experience. Use a short description when space is limited.**Note:** Ensure that the short description doesn't exceed 80 characters.

</td></tr><tr><td>

Full description

</td><td>

Full description of your app.**Note:** Ensure that the full description doesn't exceed 4000 characters.

</td></tr><tr><td>

Valid domains

</td><td>

List of valid domains for websites that your app expects to load in Microsoft Teams.**Note:** Currently only the ServiceNow domain is supported.

</td></tr><tr><td>

Version

</td><td>

Specific version of your app to track the incremental manifest submission to Microsoft Teams.For example, 1.0.0. Use a maximum of 2 digits after each decimal.

**Note:** Ensure that you put a higher number for each new version.

</td></tr><tr><td>

Accent color

</td><td>

Color to use as a background for your outline icons. **Note:** The value must be a valid HTML color code starting with a hash-tag \(\#\). For example, \#293E40.

</td></tr><tr><td>

Color icon

</td><td>

Icon of your app that you want to appear in most Microsoft Teams scenarios.You can select the following options:

-   **Use Default icon**: Changes the color of the icon back to the default color icon.
-   **Use Custom icon**: Changes the color icon with an icon color of your choice.
**Note:** Ensure that you upload only the `.png` image files that have fewer than 192x192 pixels to change the color of the icon.

</td></tr><tr><td>

Outline icon

</td><td>

Icon that is seen on the app bar when the app is in use.You can select the following options:

-   **Use Default icon**: Changes the outline icon back to the default outline icon.
-   **Use Custom icon**: Changes the outline icon with an icon of your choice.
**Note:** Ensure that you upload only the `.png` image files that have fewer than 32x32 pixels to change the outline icon.

</td></tr><tr id="message-extension"><td>

Message Extension or Copilot

</td><td>

This section allows you to activate Message extension if your bot is set up for NLU/Keyword, or activate Copilot if your bot is set up for for LLM. \(For more information on activating LLM for your bot, see [Display your chat assistant on a portal, channel, or mobile app](../../now-assist-in-va/task/display-assistant-portal-channel.md).\)-   The Message extension check box appears if you configure your bot for NLU/Keyword. Message extension lets users search and share the results through the compose message area of the Microsoft Teams client.

If you're using this bot for Microsoft Copilot, then ensure that you enable **Message Extension**. ![Now Assist in Virtual Agent conversation with Microsoft Copilot displaying the Message Extension enabled.](../images/message-extension-teams.png)

By enabling Message Extension for an app or bot, you will see the same app or bot in the message extension area while your conversation with the Now Assist using Microsoft Copilot.

-   Copilot: if you have configured your bot for LLM, this option replaces Message extension. Custom Engine Agent \(CEA\) replaces the Declarative Agent \(DA\) and allows you to use Now Assist functionality in Copilot.

The Sample Prompts window appears when you select the Copilot check box. Enter your prompts to your bot here to have the LLM follow those instructions.

![With LLM activated for your bot, Copilot replaces the Message extension option, and lets you enter prompts through a Sample Prompts window.](../images/configure-bot-copilot.png)

</td></tr></tbody>
</table>    For more details about each field, refer to [Microsoft Teams documentation](https://learn.microsoft.com/en-us/microsoftteams/platform/resources/schema/manifest-schema).

6.  Select **Save**.

    You’re redirected to the Bot configuration page where the manifest file is saved and ready for you to download.

    **Note:**

    You can also edit the manifest file by selecting **Edit configuration** on the download page and downloading the file as many times as you would like. With each new manifest, ensure that you enter a higher version number in the **Version** field so that the updated form can be saved successfully.

7.  In the Bot configuration page, under Your package, select the **Download** button to download your package file.

    **Note:**

    You can also edit the manifest file by selecting **Edit configuration** on the download page and downloading the file as many times as you would like. However, with each new manifest, ensure that you enter a higher version number in the **Version** field so that the updated form to be saved successfully.


## What to do next

[Upload the manifest package file to publish your bot](upload-package-file-msteams.md).

**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams using the self-configured bot](../concept/va-integ-teams-self-configured-bot.md)

