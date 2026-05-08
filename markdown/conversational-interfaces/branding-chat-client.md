---
title: Branding your chat client
description: Customize your chat interface with your own brand, including company logo and bot avatar, UI color schemes, fonts, and the chat support menu displayed to your users.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Branding, chat, client, customize, interface, brand, Microsoft Teams, Facebook, Messenger, Conversational Integration, Virtual agent]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Branding your chat client

Customize your chat interface with your own brand, including company logo and bot avatar, UI color schemes, fonts, and the chat support menu displayed to your users.

**Note:** For new customers onboarding from Vancouver onward, the chat widget is only accessible to authenticated users by default. To allow unauthenticated users to access the chat widget, enable **Public access** in **Conversational Interfaces** &gt; **Settings** &gt; **General**. For more information, see [Enable public access to the chat widget](../task/enable-public-access-web-client.md).

## Multiple branding configurations

You can create any number of branding configurations for an instance. These branding configurations apply to the web chat and mobile clients and don't apply to the Conversational Integrations for Slack, Microsoft Teams, Workplace by Facebook, and Facebook Messenger.

**Note:** Branding for bots in the Conversational Integration with Microsoft Teams is available through the Microsoft Teams app customization feature. For details, see [MS Teams branding for the conversational integration](https://community.servicenow.com/community?id=community_article&sys_id=3b4f487edbe17490904fa9fb1396195b) in Now Community. For information about branding bots in Slack, see [Configure branding for your Virtual Agent bot in Slack](../../virtual-agent/task/slack-branding-overview.md).

The default branding configuration includes the Virtual Agent bot, which has a ServiceNow avatar. If you want additional branded bots, create a user profile for each bot in the User \[sys\_user\] table. Give your bot a unique user ID, name \(for example, Acme\), upload the photo \(image\) for your bot avatar, and make your bot active. For details on adding users to your instance, see Create a user.

Once created, you then select the bot to be used in a configuration. A branded bot can be used in a single configuration or in multiple branding configurations.

## Supported branding items

Conversational Interfaces provides a default branding configuration that you can customize. To change the default configuration, create other branding configurations, or modify the chat \(support\) menu, gather and prepare the following files and information:

-   **Organization images**

    Images of company logos to be used in your chat windows. If you're using Virtual Agent, the images of avatars to be used for branded bots.

    Images must be in .jpg, .png, .bmp, .gif, .jpeg, .ico, or .svg file format. The images can be high resolution, but the image display is scaled based on the aspect ratio. Keep in mind that if chat is run in its own browser window, a thumbnail of the branding logo displays automatically in the browser tab.

-   **Colors and fonts**

    Colors and fonts used for the various user interface items, such as chat bubbles, buttons, and notifications displayed.

    If you want to change the color of interface items, determine the Hex number or RGBA color for those items. When you specify the Hex or RBGA colors during configuration, you can immediately see your changes in the example chat window. To learn more about Hex numbers and RGB color specifications, see [HTML Color Names \(W3CSchools\)](http://www.w3schools.com/tags/ref_colornames.asp).

    ![UI features in the chat window include the logo, menu icon, avatar, bot bubble, timestamp, chat background, user bubble, etc.](../image/chat-window-labels.png "UI items in the chat window")

    1.  Logo and chat header
    2.  Menu icon
    3.  Avatar
    4.  Bot bubble
    5.  Timestamp
    6.  Chat background
    7.  User bubble
    8.  Category background
    9.  Link text
    10. Button background
    11. Input background
-   **Chat menu items**

    Contact information for your support organization, such as support call hours, call center support phone number, and support email address. You can customize information in the support menu by adding or changing menu items, including the text and icons displayed. You can also control the visibility of the menu items \(show or hide menu options\).

    You can also change the default menu icons or add icons for new menu items. The icons must be in .svg file format. For better resolution, use a single-color icon.

    ![The chat menu includes the menu title, menu icon, menu label, and a toggle switch to enable audible alerts.](../image/support-menu-callouts.png "Chat menu")

    1.  Menu title
    2.  Menu icon
    3.  Menu label
    4.  Audible alert enabled for Virtual Agent chats
    5.  \(not shown\) Wait time display if a live agent is available

-   **[Create a new user for a branded bot](../task/ci-create-new-branded-bot.md)**  
The default branding configuration includes the Virtual Agent bot, which has a ServiceNow avatar. To create a new bot with your own branding, create an active user profile for the bot and link it to a Live Profile.
-   **[Set up your Virtual Agent bot's branding](../task/ac-configure-chat-branding.md)**  
Create different Virtual Agent branding configurations for the various organizations that use your instance. These configurations apply to the web-based chat and mobile clients only.

**Parent Topic:**[General chat settings](ci-configuring-chat-features.md)

