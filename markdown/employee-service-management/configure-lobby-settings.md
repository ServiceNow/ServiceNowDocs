---
title: Configure Lobby Settings
description: You can override the lobby settings in your instance to allow the participants to join the conference call without waiting in the lobby.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Configure Lobby Settings

You can override the lobby settings in your instance to allow the participants to join the conference call without waiting in the lobby.

## Before you begin

**Note:** This is an additional configuration, which is optional and can be used as required.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Microsoft Teams** &gt; **Configuration**.

    ![Notify settings](../image/sn-notify-settings.png)

    **Note:** In the **Setup** tab, ensure that **Enable create online meeting** option is selected.

    ![Enable create online meeting option](../image/enable-create-online-meeting.png)

2.  Select **Override Lobby settings** option.

    ![Override Lobby settings tab](../image/override-lobby-settings-tab.png)

    The **Lobby Bypass Settings** tab appears once you select the **Override Lobby settings** option.

3.  Select **Audio Conferencing** tab, and then select **Enable Audio Conferencing**option.

    **Note:** If you have an Microsoft Azure audio conferencing subscription, you must enable this option to enable the users to join the conference call via phone numbers.

    ![Enable audio conferencing option](../image/enable-audio-conf-01.png)

4.  Select **Lobby Bypass Settings** tab.

    ![Lobby bypass settings tab](../image/lobby-bypass-settings.png)

    1.  **Who can Bypass Lobby**: Select the participants who can automatically join the conference call.
    2.  **Allow dial-in users to bypass the lobby**: This option appears only if **Enable Audio Conferencing** option is selected in **Audio Conferencing** tab. Select this option to allow the participants to automatically join the conference call if they have joined using the conference bridge number.
5.  Select **Update**.


**Parent Topic:**[Configure Notify connector for Microsoft Teams](../concept/config-notify-ms-teams.md)

