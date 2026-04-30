---
title: Configure Microsoft Teams as virtual meeting provider
description: Set Microsoft Teams as your virtual meeting provider.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Teams as virtual meeting provider

Set Microsoft Teams as your virtual meeting provider.

## Before you begin

-   Ensure the following:
    -   Update the Workplace Reservation Management application only after installing the Microsoft Teams spoke. Otherwise, you must repair the Workplace Reservation Management application.
    -   Microsoft Teams works only with a Microsoft account \(Exchange Online, Exchange OnPrem\). If you have both Google and a Microsoft Teams account, the virtual meeting provider cannot be added. If you want to create a Microsoft Teams account, you must create a Microsoft account. The Microsoft Teams account is mapped to the Microsoft account and not to the Google account.
    -   For Microsoft Teams, to create a meeting link on behalf of other users, refer to [Microsoft documentation](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy/).

The Workplace Reservation Management application provides the **Template** virtual meeting provider by default. After you setup a connection between Workplace Reservation Management and Microsoft Teams, the system, by default, provides the **Microsoft Teams** virtual meeting provider configured with the following flows:

|Field|Flow|
|-----|----|
|Create meeting|`Create Microsoft Teams Meeting`|
|Get meeting details|`Get MS Teams Thread ID`|
|Get recording|`Get Microsoft Teams Recording`|

For more information on how to create a flow, refer to [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Important:** The virtual meeting providers are deactivated by default. Change the **Active** status of the desired virtual meeting provider to **true** to start using.

Role required: sn\_wsd\_rsv.admin

## Procedure

1.  Connect Workplace Reservation Management and Microsoft Teams.

    To create a connections, refer to [Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md).

    After the connection is configured, the application by default provides with the **Microsoft Teams** virtual meeting provider.

2.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Virtual Meeting Providers**.

3.  Select **Microsoft Teams**.

4.  On the form, to activate, select the **Active** check box.


## Result

Microsoft Teams is set as the virtual meeting provider.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

