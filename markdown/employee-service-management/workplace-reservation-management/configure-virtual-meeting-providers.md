---
title: Configure virtual meeting providers
description: Enable employees to provide a virtual meeting link with their reservation. Configure the virtual meeting providers so that the virtual meeting link of that provider is automatically generated when the employee makes a reservation.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure virtual meeting providers

Enable employees to provide a virtual meeting link with their reservation. Configure the virtual meeting providers so that the virtual meeting link of that provider is automatically generated when the employee makes a reservation.

## Before you begin

The Workplace Reservation Management application provides the **Template** virtual meeting provider by default. The following virtual meeting providers are also supported if they are configured:

-   Microsoft Teams: Refer to [Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md). Microsoft Teams.
-   Zoom: To use Zoom, you must have a Zoom user account. Refer to [Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md).

    **Warning:** The Zoom spoke version 3.0.0 is not supported. Only the Zoom spoke versions 3.0.3 and later are supported.

-   Ensure the following:
    -   Update the Workplace Reservation Management application only after installing the Microsoft Teams and Zoom spokes. Otherwise, you must repair the Workplace Reservation Management application.
    -   Microsoft Teams works only with a Microsoft account \(Exchange Online, Exchange OnPrem\). If you have both Google and a Microsoft Teams account, the virtual meeting provider cannot be added. If you want to create a Microsoft Teams account, you must create a Microsoft account. The Microsoft Teams account is mapped to the Microsoft account and not to the Google account.
    -   For Microsoft Teams, to create a meeting link on behalf of other users, refer to [Microsoft documentation](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy/).

**Important:** The virtual meeting providers are deactivated by default. Change the **Active** status of the desired virtual meeting provider to **true** to start using.

To configure a virtual meeting provider, you must have the following flows already created to use for the virtual meeting provider:

-   Create meeting
-   Cancel meeting
-   Get meeting details
-   Update meeting
-   Get recording

For more information on how to create a flow, refer to [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

Role required: sn\_wsd\_rsv.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Virtual Meeting Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the virtual meeting provider.|
    |Create meetings|Flow to create a meeting.|
    |Cancel meeting|Flow to cancel the meeting.|
    |Get meeting detail|Flow to get the meeting details.|
    |Provider identifier|URL that must be used to validate the generated meeting links. When a meeting is created in the employee's calendar provider, the specified URL is used to validate the meeting link during the synchronization with Workplace Reservation Management.|
    |Application|Application for which you are adding the virtual meeting provider. This field is automatically set. Ensure that **Workplace Reservation Management** is selected.|
    |Update meeting|Flow to update the meeting.|
    |Get recording|Flow to get the recording of the meeting.|
    |Order|Order in which the virtual meeting provider must appear.|
    |Active|Option to activate the virtual meeting provider.|

4.  Click **Submit**.


## Result

The virtual meeting provider is added. To enable employees to add a virtual meeting link along with their reservation, select the **Virtual meeting provider** option in the Reservable module.

**Note:** When a reservation includes a virtual meeting link, then the meeting link will appear as follows when it is synced with the Microsoft Outlook calendar provider of the attendees:

-   Zoom: If a Zoom meeting link is added, the link appears in the **Location** field of the email containing the meeting invite.
-   Microsoft Teams: When a reservation is created with a virtual meeting link, the application retrieves the meeting link and the joining-related details and saves them on the reservation record. When this reservation is synchronized with Microsoft Outlook calendar, the meeting link and the joining-related details are added to the body of the calendar event. Similarly, when a reservation is created in the Microsoft Outlook calendar using the **Teams meeting** toggle button, the meeting link is retrieved and saved as a virtual meeting link on the reservation record.

    **Note:** As the meeting link appears in the body of the email, in any case, if you want to update or change the meeting details, you must do it only using the Workplace Reservation Management. Because when a reservation synchronization is performed, the details \(in this case, the meeting link and details\) are synchronized only in one way, that is, from Workplace Reservation Management to the calendar provider\(in this case Microsoft Teams\). If you already made any changes to the meeting details or the notes from the calendar provider, it is overwritten by Workplace Reservation Management when a synchronization is performed. For more information, refer to [Explore Workplace Calendar Synchronization](../../workplace-calendar-synchronization/concept/workplace-calendar-synchronization-overview.md).

-   **Any other virtual meeting providers**: The meeting link is added in the **Location** field of the email containing the meeting invite.

For the meeting link to appear as above, the following plugin versions are required:

-   Microsoft Exchange Online spoke version 3.5.0 and later.
-   Microsoft Teams Communications spoke version 1.3.0 and later.
-   Latest version of Workplace Reservation Management application.

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

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

