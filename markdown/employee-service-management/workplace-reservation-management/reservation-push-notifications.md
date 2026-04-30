---
title: Mobile push notifications for workplace reservations
description: As a workplace admin, you can configure push notifications that you want to send to an employee on their mobile devices to alert them about important events and enable them to perform an action.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workplace Reservation Management references, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Mobile push notifications for workplace reservations

As a workplace admin, you can configure push notifications that you want to send to an employee on their mobile devices to alert them about important events and enable them to perform an action.

To configure mobile push notifications, refer to [Mobile push notifications](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

As an employee, to receive push notifications, you must have the following:

-   Push notifications are enabled by your organization.
-   Following plugins:
    -   Workplace Reservation Management
    -   Workplace Service Delivery for Mobile version 1.5.1.

        Workplace Service Delivery for Mobile version 1.5.1 supports the Tokyo family release. If you are using Workplace Service Delivery for Mobile version 1.3.4 or earlier versions, it is not possible to receive any push notifications.

-   You must be logged in on your mobile.

Push notifications are sent for events such as, when a reservation is created or updated on your behalf, or when a reservation is required to check in or check out.

-   The push notifications are triggered by the following scheduled jobs when there are any upcoming events.
    -   **Check-in/out reminder**: The schedules job runs periodically and sends out notifications regarding upcoming reservation check in and check out. The scheduled jobs uses the **sn\_wsd\_rsv.time\_before\_check\_in\_out\_reminder** and **sn\_wsd\_rsv.time\_when\_reservation\_cancelled\_without\_check\_in** system properties for the time intervals.
    -   **Trigger mobile push notifications for upcoming reservation events**: The schedules job runs periodically and sends out notifications regarding upcoming reservation events.
-   The system also sends actionable push notifications with actions such as **Check-In** and **Check-Out** to the mobile devices.
-   Notifications are sent in English.
-   Push notifications are sent on iOS and Android mobile devices.

## Push notifications scenarios

As an employee, you will receive push notification for the following scenarios:

-   **Reservation is ready for check in**

    An actionable push notification is received that you can check in the reservation. You can check in the reservation directly from the notification by selecting the **Check-In** option. After the selection, the reservation is checked in and you are navigated to the reservation details page.

-   **Reservation check in about to start in a few minutes**

    Push notification is received that you can check in the reservation in a few minutes.

-   **Reservation is created for you by someone**

    Push notification is received that a reservation is created for you by someone on your behalf.

-   **Reservation about to start**

    Push notification is received that the reservation is about to start.

-   **Reservation cancelled due to check in delay**

    Push notification is received that the reservation is cancelled as it was not checked in on time.

-   **Reservation created for you by someone is updated**

    Push notification is received that the reservation made on your behalf by someone has been updated.

-   **Reservation about to end**

    Push notification is received that the reservation is about to end.

-   **Reservation is ready for check out**

    An actionable push notification is received that you can check out the reservation. You can check out the reservation directly from the notification by selecting the **Check-Out** option. After the selection, the reservation is checked out and you are navigated to the reservation details page.

-   **Reservation started but pending check in**

    Push notification is received that you are yet to check in the reservation even after the reservation start time.

-   **Reservation ended but pending check out**

    Push notification is received that you are yet to check out the reservation even after the reservation time has started.


**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](components-installed-with-wsd-reservation-mgmt.md)

[Properties installed with Workplace Reservation Management](properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](proximity-calculation-for-browse-near-person.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Location privacy settings and impact](location-privacy-settings-and-impact.md)

[Additional details record producer - Mapping Variable types and limitations](custom-fields-record-producer-mapping-variable-type-conditions.md)

