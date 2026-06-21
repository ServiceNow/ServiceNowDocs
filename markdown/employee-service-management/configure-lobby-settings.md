---
title: Configure Lobby Settings
description: You can override the lobby settings in your instance to allow the participants to join the conference call without waiting in the lobby.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/configure-lobby-settings.html
release: xanadu
product: Employee Service Management
classification: employee-service-management
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

    \[Omitted image "sn-notify-settings.png"\] Alt text: Notify settings

    **Note:** In the **Setup** tab, ensure that **Enable create online meeting** option is selected.

    \[Omitted image "enable-create-online-meeting.png"\] Alt text: Enable create online meeting option

2.  Select **Override Lobby settings** option.

    \[Omitted image "override-lobby-settings-tab.png"\] Alt text: Override Lobby settings tab

    The **Lobby Bypass Settings** tab appears once you select the **Override Lobby settings** option.

3.  Select **Audio Conferencing** tab, and then select **Enable Audio Conferencing**option.

    **Note:** If you have an Microsoft Azure audio conferencing subscription, you must enable this option to enable the users to join the conference call via phone numbers.

    \[Omitted image "enable-audio-conf-01.png"\] Alt text: Enable audio conferencing option

4.  Select **Lobby Bypass Settings** tab.

    \[Omitted image "lobby-bypass-settings.png"\] Alt text: Lobby bypass settings tab

    1.  **Who can Bypass Lobby**: Select the participants who can automatically join the conference call.
    2.  **Allow dial-in users to bypass the lobby**: This option appears only if **Enable Audio Conferencing** option is selected in **Audio Conferencing** tab. Select this option to allow the participants to automatically join the conference call if they have joined using the conference bridge number.
5.  Select **Update**.


**Parent Topic:**[Configure Notify connector for Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/config-notify-ms-teams.md)

