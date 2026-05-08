---
title: Create a new user for a branded bot
description: The default branding configuration includes the Virtual Agent bot, which has a ServiceNow avatar. To create a new bot with your own branding, create an active user profile for the bot and link it to a Live Profile.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual Agent, branded, bot, avatar, Live Profile, live\_profile]
breadcrumb: [Branding your chat client, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Create a new user for a branded bot

The default branding configuration includes the Virtual Agent bot, which has a ServiceNow avatar. To create a new bot with your own branding, create an active user profile for the bot and link it to a Live Profile.

## Before you begin

Role required: admin

## About this task

If you want to create a new branded bot, create an active user profile for each bot in the User \[sys\_user\] table. Then create a bot profile record by adding this user to the Live Profile \[live\_profile\] table.

## Procedure

1.  Create a user for the bot.

    Include an image \(avatar\) for your bot when you create the user. Also ensure that the user is active.

2.  Navigate to **All**, and then enter `live_profile.list` in the filter.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_mky_2ts_stb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the bot profile.

</td></tr><tr><td>

Type

</td><td>

Type of live profile. Select **User**.

</td></tr><tr><td>

Document

</td><td>

Table associated with the profile.1.  Select the Search icon ![Search icon.](../../virtual-agent/images/icon-search.png).
2.  In the Select the document dialog box, specify the following information:
    -   **Table name**: Select **User \[sys\_user\]**.
    -   **Document**: Select the name of the user you created for the bot.
3.  Select **OK**.


</td></tr><tr><td>

Photo

</td><td>

Image \(avatar\) for the bot profile.

</td></tr><tr><td>

Description

</td><td>

Text that describes the live profile.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

You can associate the bot profile with a new branding configuration. For details, see [Set up your Virtual Agent bot's branding](ac-configure-chat-branding.md).

**Parent Topic:**[Branding your chat client](../concept/branding-chat-client.md)

