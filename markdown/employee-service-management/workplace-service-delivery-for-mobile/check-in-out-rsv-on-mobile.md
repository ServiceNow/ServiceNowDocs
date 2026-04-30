---
title: Check in or check out a reservation
description: Check in an upcoming reservation or check out an ending reservation using the Now Mobile app.
locale: en-US
release: yokohama
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-04-29"
reading_time_minutes: 2
breadcrumb: [Use, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Check in or check out a reservation

Check in an upcoming reservation or check out an ending reservation using the Now Mobile app.

## Before you begin

If you have occupancy sensors installed in your workplace location, your reserved spaces are automatically checked in. You also receive a push notifications on Workplace Service Delivery for Mobile app when your reserved spaces are checked in automatically. If the workplace location or space state is **Occupied**, then, application automatically checks in the reservation. The reservation state moves to In progress state. A push notification is sent to Workplace Service Delivery for Mobile "Your reservation has started. You are automatically checked in based on the presence detected at the space. No further action is required." If the state of the space is **Unoccupied** or **Invalid**, application sends push notification "Your reservation for Reservation for &lt;space-name&gt; has started. Either Check in to confirm your attendance or Release Booking to Cancel the space reservation". For more information, see [Configure automatic check-in for reserved spaces](../../wsd-reservation-management/concept/configure-rsv-check-in.md).

**Note:** Reservation check-in and check-out is currently not supported for multi-location reservations \(combining two or more reservations into one reservation\). Check-in or check-out of reservations with multiple locations for the same date and time and with the same reservation owner is not allowed by the application. In case of group reservations, each space is assigned to a different employee, check-in for group reservations is also not allowed in bulk. You have to check-in a reservation one at a time.

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  On your mobile device, open the Now Mobile app.

2.  In the Workplace Reservations section, tap **My reservations**.

    You can also open the My reservations section by selecting the services icon \(![Services icon.](../images/services-app.png)\).

3.  Select the reservation that you want to check in or check out.

4.  To check in or check out, do one of the following:

    -   To check in the reservation, tap **Check in reservation**.
    -   To check out the reservation, tap **Checkout reservation**.

        **Note:** You can check out a reservation only after you check in. After you check out the reservation, the status of the reservation is shown as **Complete**.


## Result

The reservation is checked in or checked out accordingly.

**Parent Topic:**[Using Workplace Service Delivery for Mobile](../concept/using-wsd-mobile.md)

**Previous topic:**[Edit or cancel a reservation on Now Mobile app](edit-rsv-on-mobile.md)

**Next topic:**[Share your reservation details with other users](share-rsv-details.md)

