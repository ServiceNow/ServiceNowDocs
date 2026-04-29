---
title: Configure branding for your Virtual Agent bot in Slack
description: You have the flexibility to customize the default ServiceNow branding for your Slack Virtual Agent. You can change the production bot's name and icon.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Configure, branding, virtual agent, bot, slack, com.glide.cs.enable\_slack\_branding]
breadcrumb: [Configure VA settings for Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure branding for your Virtual Agent bot in Slack

You have the flexibility to customize the default ServiceNow branding for your Slack Virtual Agent. You can change the production bot's name and icon.

## Before you begin

Role required: admin or virtual\_agent\_admin

**Note:** The branding capability in Slack is available from the August 2022 store release and is compatible with the Tokyo release and above. Users must ensure that they are on the Tokyo family release and have downloaded the August store release for the Conversational Integration with Slack app to use this functionality.

Ensure that you set the **com.glide.cs.enable\_slack\_branding** system property to true before configuring the branding settings for your bot.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  On the **General Settings** page under **Channels and integrations**, select **View All**.

3.  On the Channels and integrations page, in the Slack tile, select **Manage**.

4.  Select the Manage Bot icon and select **Manage Virtual Agent**.![The Manage Virtual Agent option displays on the Manage bot menu for the Slack channel.](../images/manage-slck-snow-bot.png)

5.  On the Branding tab, provide the following details:

    -   **Bot name**: Name that appears on the Slack conversation body.

        On the Configure your bot integration in Slack page, change the default bot name to a bot name of your choice and select **Save**.

        **Note:**

        -   If you ever want to change the bot name back to the default bot name, delete the bot name that you provided and select **Save**. The bot name will be taken from the available bot name on Slack admin center.
        -   If you want your bot name to be different from the header and the left pane, provide a different name.
    -   **App name**: Name that appears in the Slack header and left panel.

        To change the App name on the Slack header and left panel, perform the following steps.

        -   Log in to [Slack admin center](https://app.slack.com/workspace-signin?redir=%2Fgantry%2Fapps-manage).
        -   Navigate to **Slack app directory** and find your Slack pre-published app.
        -   On your Slack app page, select the **Configuration** tab and navigate to the Bot User section.
        -   Select **Edit** to edit the bot name.
        -   In the Edit bot name pop-up, change the bot name to a name of your choice and select **Save Changes**.

            **Note:** If you want the bot name to be consistent with the bot name in the conversation body, then provide the same bot name.

    -   **Slack bot icon**: Icon that appears in the Slack conversation body.
        -   **Use default icon**: Select the **Use default icon** radio button and select **Save** to change the bot icon back to the default bot icon.
        -   **Use custom icon**:

            Select the **Use custom icon** radio button to change the Slack bot icon and select **Save**.

            There are two ways to upload an image icon.

            -   Select **Attach image** to browse for an image icon and select **Save**.
            -   Select the **Use image URL instead** to provide a URL of the image icon and select **Save**.
    ![In the chat window, you can modify the chat window header, the title that appears in the Slack navigation panel, and the name and icon in the conversation body.](../images/slack-branding-bot-name.png "Branded Slack conversation body")


## What to do next

Open your Slack bot interface and start a new conversation. You will notice that the bot name has been updated on the Slack conversation body, header, and in the left pane and the bot icon is updated only in the conversation body.

**Parent Topic:**[Configure Virtual Agent settings for Slack](configure-va-slack-settings.md)

