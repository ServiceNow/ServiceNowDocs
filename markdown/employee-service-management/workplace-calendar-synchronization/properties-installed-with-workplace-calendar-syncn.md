---
title: Properties installed with Workplace Calendar Synchronization
description: Customize the properties available with Workplace Calendar Synchronization.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Calendar Synchronization

Customize the properties available with Workplace Calendar Synchronization.

These properties are available for Workplace Calendar Synchronization.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_wpx_sqn_5nb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_rsvsync.sync\_integration\_mode

</td><td>

This property enables you to specify the Exchange Online sync integration mode to Strict, Personal Authentication, or Normal mode to synchronize reservation between Microsoft Exchange Online and Workplace Reservation Management.-   **Type**: string
-   **Default value**: Normal

</td></tr><tr><td>

sn\_wsd\_rsvsync.use\_user\_default\_tz

</td><td>

This property enables you to synchronize reservations created by users according to their time zone. Either the system's time zone or the user's time zone is used to update and synchronize reservation. First, the property checks if the user has a time zone specified or not. If the user has not specified any time zone, the system's time zone is used. Again, if the system has no time zone specified, then the property uses the UTC time zone.Reservations synchronized from Microsoft Exchange and Google Calendarto Workplace Service Delivery are not affected.

 -   Type: true/false
-   Default value: **false**

</td></tr><tr><td>

sn\_wsd\_rsvsync.create\_blocking\_rsv

</td><td>

This property enables you to create blocker reservations on workplace locations that are synchronized with the calendar provider.-   Type: true/false
-   Default type: **true**

</td></tr><tr><td>

sn\_wsd\_rsvsync.max\_event\_retry\_count

</td><td>

This property enables you to specify after how many times an event must be reprocessed.-   Type: Integer
-   Default value: **10**

</td></tr><tr><td>

sn\_wsd\_rsvsync.use\_default\_tz

</td><td>

This property enables you to use the default time zones during the reservation synchronization.-   Type: true/false
-   Default type: **true**

</td></tr><tr><td>

sn\_wsd\_rsvsync.exchange\_callback\_time\_limit

</td><td>

This property enables you to specify the maximum time limit to wait for Microsoft exchange to notify with a callback. Specify the time limit in negative seconds as specified in the default value.**Note:** You won’t be notified when an event is rejected or declined by Microsoft Outlook. For the same reason, a scheduled job - **Clean-up Awaiting/Rejected Reservations**, is available that you can run on any suitable frequency to clear the reservations rejected or declined by the Microsoft Outlook calendar.

-   Type: Integer
-   Default value: **-18000** \(5 hours\)

</td></tr><tr><td>

sn\_wsd\_rsvsync.outlook\_event\_sync\_interval

</td><td>

This property is used internally by the application, it enables you to set the time\(in minutes\) to synchronize events received by Microsoft Exchange with Workplace Reservation Management application. Ensure that the time that you set in this property is more that the time specified in the **Create and Update Reservations from Events** scheduled job's repeat interval.-   **Type**: Integer
-   **Default value**: 2

</td></tr><tr><td>

sn\_wsd\_rsvsync.google\_event\_sync\_interval

</td><td>

This property is used internally by the application while updating the attendee details on the reservations. Ensure that the time that you set in this property is more than the time specified in the **Update attendees of Workplace Reservation \(Google\)** scheduled job's repeat interval.-   **Type**: string
-   **Default value**: 5

</td></tr><tr><td>

sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths

</td><td>

This property enables you specify the number of months that you want a sync to run in order to sync past reservation. A single sync will run for specified number of months for past reservation. Ensure that a single sync does not return more 1000 reservations. Specify the number of months based on the same.-   **Type**: Integer
-   **Default value**: 2

</td></tr></tbody>
</table>