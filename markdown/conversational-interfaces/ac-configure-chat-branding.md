---
title: Set up your Virtual Agent bot's branding
description: Create different Virtual Agent branding configurations for the various organizations that use your instance. These configurations apply to the web-based chat and mobile clients only.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 12
keywords: [Virtual, Agent, branding]
breadcrumb: [Branding your chat client, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Set up your Virtual Agent bot's branding

Create different Virtual Agent branding configurations for the various organizations that use your instance. These configurations apply to the web-based chat and mobile clients only.

## Before you begin

If you're using ServiceNow® mobile, make sure you set up Virtual Agent for mobile chat. For details, see [Configure Virtual Agent for a ServiceNow mobile application](../../virtual-agent/task/configure-va-mobile-web-client.md).

Check for updates and improvements to the Omni-Experience Standard Feature Set application on the ServiceNow Store.

**Note:** Branding for bots in the Conversational Integration with Microsoft Teams is available through the Microsoft Teams app customization feature. For details, see [MS Teams branding for the conversational integration](https://community.servicenow.com/community?id=community_article&sys_id=3b4f487edbe17490904fa9fb1396195b) in Now Community. Branding for bots in Slack is available as well. For details, see [Configure branding for your Virtual Agent bot in Slack](../../virtual-agent/task/slack-branding-overview.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under the **Display Options** section, select **View All** next to **Branding**.

3.  Select **New** to create a branding configuration or select the branding configuration record to be updated.

4.  On the form, fill in the fields.

<table id="table_epv_csw_gjb"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td id="branding-names">

Branding name

</td><td>

Name of the branding configuration.Create a new branding configuration or select one of the available choices. For the Xanadu release, the choices include:

-   Polaris-Dark
-   Polaris-Light


</td></tr><tr><td>

Chat Header

</td><td>

Text string that identifies your company or organization in the chat window header. For example: Acme Support.

</td></tr><tr><td>

Minimum delay between bot messages \(ms\)

</td><td>

Minimum delay, in milliseconds \(ms\), that occurs between bot responses. The default delay is 500 ms.

</td></tr><tr><td>

Minimum delay before displaying typing animation \(ms\)

</td><td>

Minimum delay, in milliseconds \(ms\), that occurs before showing the animation ellipsis indicating the bot is processing user input.

</td></tr><tr><td>

Menu Title

</td><td>

Name of the support menu. The default title is Contact Support.

</td></tr><tr><td>

Branding key

</td><td>

Read-only sys\_id of the configuration, which reflects the **Branding name** you entered. The key is in lower case letters with spaces replaced by underscore characters.

</td></tr><tr><td>

Button Selection Text

</td><td>

Font color of the **New messages above** or **New messages below** buttons.

</td></tr><tr><td>

Bot Profile

</td><td>

List that opens the Live Profile form to select or create a new bot user profile, which includes the bot picture \(avatar\). This bot picture appears in the chat messages.-   To review and edit the Virtual Agentor Now Assist bot profile, select the information icon.
    -   To change the bot picture or description, select **Edit record** in the message at the top of the page.
    -   In the Live Profile form, modify the fields and select **Update**.
-   To choose or change the bot for the configuration, select the search icon and select the **Bot Profile** field. Choose the bot profile that you created in a previous step.


</td></tr><tr><td>

Chat Header Logo

</td><td>

Logo image that displays in the chat header. If live chat is run in a browser window, the logo also displays in the browser tab. The chat header logo is set to 42x42 pixels, and the chat message logo is set to 24x24 pixels. An uploaded image that is smaller than these dimensions will appear stretched. A larger image will be scaled down. -   To add a logo, select **Attach Image** and use the file finder to choose the image.
-   To change the logo, select **View image**. From the file finder, select the new logo file and select **OK**. The updated logo displays below this field.
-   To remove the logo, select the trash icon. The file is immediately deleted.


</td></tr><tr><td>

Enable showing the 'New Messages Below' or 'New Messages Above' notification

</td><td>

Select this option to display notifications for new messages below or above your current view of the chat.

</td></tr></tbody>
</table>5.  Select **Save**.

    From here, you can adjust the color, icons, and font type and size of the chat client to match your brand. For example, you can:

    -   [Change the color of items](ac-configure-chat-branding.md#ul_b3w_xsv_jvb)
    -   [Customize the icons](ac-configure-chat-branding.md#customize-icons)
    -   [Customize the fonts used in the chat](ac-configure-chat-branding.md#customize-fonts)
6.  To change the color of items in the chat window, select the **Colors** tab.

    ![Chat branding colors tab showing chat window and chat messages colors.](../image/chat-branding-colors-tab.png)

    Select an item and specify the Hex or red blue green alpha \(RGBA\) colors you want to use for that item. When you do so, the example chat window shows a preview of your changes.

    |Label|Description|
    |-----|-----------|
    |Chat window|
    |Chat Header Background|Background color of the chat header.|
    |Chat Background|Background color of the chat window.|
    |Menu Icon|Color of the menu icon, which provides user options to end a conversation or contact customer support.|
    |Chat Header Font|Font color of text in the chat header.|
    |Input Background|Background color of the user input bar.|
    |Chat messages|
    |User Bubble Background|Background color of the user chat bubble.|
    |Agent Bubble Background|Background color of the live agent chat bubble.|
    |Bot Bubble Background|Background color of the bot chat bubble.|
    |Link|Color of links presented in the conversation.|
    |Button Background|Background color of buttons used in the conversation.|
    |Notification Background|Background color of Virtual Agent notifications delivered in the web chat client.|
    |User Bubble Font|Font color of text in the user chat bubble.|
    |Agent Bubble Font|Font color of text in the live agent chat bubble.|
    |Bot Bubble Font|Font color of text in the bot chat bubble.|
    |Link turned off|Color of links turned off in the conversation.|
    |Notification Text|Font color of Virtual Agent notifications delivered in the web chat client.|
    |Others|
    |System message|Color of general system messages displayed in the conversation.|
    |Category background|Background color of the heading above a list of topics.|
    |Separator|Color of the dashed line that separates each conversation in the Preview window.|
    |Time Stamp|Color of the timestamp displayed when significant activity occurs during a conversation, such as a record being created.|
    |Category font|Font color of text in the category heading.|
    |Loading Animation|Color of the animated dots that indicate the system is processing information.|

7.  To customize the chat icons in the chat window, select the **Icons** tab.

    ![Chat branding Icons tab showing main chat window and all topics window icons.](../image/chat-branding-new-tabs.png)

    You can customize the icons on four different chat screens: the main chat screen, the all topics screen, the support menu, and the end conversation screen. Use this tab to do the following:

    -   Add a custom icon: Select **Add** for the icon, and then select **Attach image**. After choosing the image file, select **Apply**.
    -   Replace a custom icon: Select **Replace** for the icon. Select the trash can icon to delete the current image, and then upload a new one.
    -   Revert to the system default icon: Select **Remove** for the icon.

        **Note:** You can't remove system default icons.

    When you specify the icons during configuration, the example chat window shows a preview of your changes.

    **Note:** Unlike other settings on the branding page, icon changes take effect on the chat widget as soon as you select **Apply**. Other changes don't take effect until you select **Save** at the top of the page.

    Valid file formats are .jpg, .png, .bmp, .gif, .jpeg, .ico, and .svg.

8.  Customize the font type and font size.

    The available branding configurations \(for example, Polaris-Light or Polaris-Dark\) are located [here.](ac-configure-chat-branding.md#table_epv_csw_gjb)

    **Note:** This feature is only available after you've installed and updated the Omni-Experience Standard Feature Set to the latest version through the ServiceNow® Store.

    To customize the fonts shown in the chat, select the **Fonts** tab.

    To change the font type, choose one of the following methods:

    1.  Select the fonts you want to use.

        From the **chat header text** drop-down list, select the font you want to use for the header.

        Do the same for the **chat body text.**

        You will see an example of the new font.

    2.  Download the fonts from a URL.

        From the **Add custom font** drop-down list, select **From URL**, specify the URL, and apply the changes.

    3.  Upload the fonts you want to add from an attached file.

        From the **Add custom font** drop-down list, select **Upload font**, specify the path to the file you want to attach, and apply the changes.

    To change the font size for the chat header and the chat body, do the following:

    1.  From the **Font body size** dropdown, choose the Regular, Large, or Extra Large font size.

    2.  From the **Font header size** dropdown, choose the Regular, Large, or Extra Large font size.

        **Note:** These changes do not apply to custom controls you have added to the chat widget. Custom controls must be updated separately.

    3.  Preview the changes in your chat window on your portal or website.

9.  To update the Contact support menu, scroll down to the **Menu Items** section.

    ![Chat branding menu items section, showing chat, email, and phone contact items.](../image/chat-branding-menu-section.png)

    You can change the icons, labels, visibility, and display order of the Email, Chat, and Phone menu items. You can also add custom options to the menu.

    1.  In the **Menu Items** section, do any of the following:

        -   To edit a menu item, select the record icon.
        -   To add a new menu item, select **New**.
        -   To delete a menu item, select the record icon. In the record, select the More Actions icon ![More Actions icon.](../../virtual-agent/images/icon-more-actions.png), and then select **Delete**.
        For each menu entry, fill in the fields.

<table id="table_t21_dx1_krb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Text string that describes the menu type.The labels for the default menu types in the Global application scope are:

-   Email - Option that opens the default email. Default label: **Send Email to Customer Support**
-   Chat – Option for chatting with a live agent. Default label: **Contact Live Agent** for Chat type
-   Phone - Option that indicates when phone support is available. Default label: **Call Support—\(Daily 5AM - 11PM\)**
The label text can be up to 75 characters in length.

</td></tr><tr><td>

Type

</td><td>

Type of menu item. For example, if you're adding a menu item that is a link to specific information such as a help page, select the `Link` Type.The menu item types are:

-   Email: Option for contacting support through email.
-   Link: Option for a link to a web page
-   Chat: Option for contacting a live agent through chat.
-   Text: Option for setting a text string
-   Phone: Option for contacting support by phone


</td></tr><tr><td>

Value

</td><td>

The menu type value. For example, the **Value** for Email is the email address of the support group.The values for the default menu types are:

-   Email: Email address of the support group. For example: support@example.com.
-   Phone: Phone number of your call support organization.
-   Email: Email address of your support organization.
**Note:** The chat menu type doesn't have a value.

</td></tr><tr><td>

Visible

</td><td>

Option that makes the item visible in the Contact support menu.

 Clear this option to hide the menu item.

</td></tr><tr><td>

Display default icon

</td><td>

Option that indicates the default icon for the item is visible in the menu.Clear this option to add, change, or delete a menu icon.

 -   To add an icon for a new menu item, select **View image**. From the file finder, choose your icon file and select **OK**. The uploaded icon displays below the **Icon** field.
-   To change an icon, in the **Icon** field select **Update**. From the file finder, select the new logo file and select **OK**. The updated Icon displays below this field.
-   To remove the icon, select **trash** icon. The file is immediately deleted.


</td></tr><tr><td>

Order

</td><td>

Number that identifies the sequence in which the item appears in the Contact support menu. The number 1 indicates that the item is the first option listed in the menu.

</td></tr><tr><td>

Application

</td><td>

Global.

</td></tr></tbody>
</table>    2.  When you complete the **Menu Item** section for a menu type, select **Save**.

10. Do one of the following to apply the branding configuration:

    -   Apply the branding configuration to a Service Portal Agent Chat Configuration. In the server script that passes page and widget data to an Agent Chat \(Virtual Agent or Live Agent\) conversation, specify the branding key to be used. Items passed in this script are available to all pages in the portal. For details on setting up Service Portal Agent Chat, see [Add your bot to a portal](ac-configure-bot-portal.md).

        For example, the following Service Portal Agent Chat Configuration for the Knowledge Portal uses the chat branding key, `custom_1`.

        ![Service Portal Agent Chat Configuration record example.](../image/va-sp-chat-config.png)

        **Note:** There are other Service Portal Agent Chat features that you can configure, such as [customizing the Agent Chat button](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) in your portal. For more information on customizing the Agent Chat widget in Service Portal, see [Configure Agent Chat in Service Portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    -   Apply the branding configuration to a destination page. Enter the system parameter `sysparm_branding_key` with the branding key in the chat widget URL. For example:

        `https://<*your-instance-name*>service-now.com/$sn-va-web-client-app.do?sysparm_branding_key=acme`

        In this example, `acme` is the key of the branding configuration to be used.

    -   Apply the branding configuration to an embedded chat widget. Enter the system parameter `sysparm_branding_key` with the branding key in the URL for the embedded chat widget. For example:

        `https://<*your-instance-name*>service-now.com/$sn-va-web-client-app_embed.do?sysparm_branding_key=acme`

        In this example, `acme` is the key of the branding configuration to be used.

11. If you're using [Conversation Autopilot](../concept/ci-agent-chat-using.md#) with your branded bot, specify the branded bot name displayed in the chat window during Autopilot sessions by changing system properties as follows.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    2.  Under the **System actions** section, select **View All** next to **System messages**.

    3.  Change the **Value** field of the **com.glide.cs.autopilot.client\_initiated\_header** system property to specify the branded bot name instead of the Virtual Agent bot name displayed in the header of the chat window.

        ![Bot name highlighted in header of chat window during Conversation Autopilot session.](../image/autopilot-header.png "Autopilot header in chat window")

    4.  Update the **com.glide.cs.autopilot.client\_initiated\_message** system property to specify the branded bot name displayed to the requester during the conversation.

        ![Message displayed in the chat window informing the user that the Agent has enabled Virtual Agent to help complete the task.](../image/autopilot-msg-chat-window.png "Autopilot message during the conversation")


**Parent Topic:**[Branding your chat client](../concept/branding-chat-client.md)

