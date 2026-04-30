---
title: Properties installed with Workplace Reservation Management
description: Properties available with Workplace Reservation Management.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2025-12-07"
reading_time_minutes: 5
breadcrumb: [Reference, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Reservation Management

Properties available with Workplace Reservation Management.

These properties are available for Workplace Reservation Management \(**All** &gt; ****Workplace Reservation Management**Administration** &gt; **Properties**\).

**Note:** These properties are also listed in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation context-menu filter.

<table id="table_cqn_gcl_kmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_rooms.default\_page\_size

</td><td>

This property enables you to specify the number of reservable entries displayed on a page. This value is used on the following pages:-   On the Search page while loading reservable items.
-   On the Reservation summary page while loading sibling occurrence.
-   On the My reservations page.

 If an incorrect value is configured in the widget, the value specified in this property is used as a default value.

-   Type: Integer
-   Default value: **8**

</td></tr><tr><td>

sn\_wsd\_rsv.enable\_auto\_search

</td><td>

This property controls auto-search capability on the reservation portal while creating a reservation.By default, this property value is set to false. If set to true, the search button is not visible on the Advanced reservation portal page and the space details page. An auto search is triggered when one of the following information is changed in the reservation:-   Building
-   Floor.
-   Start Date.
-   End Date.
-   All day option is enabled.
-   Recurring \(Daily/Weekly, Monthly, and For/Until\) is enabled.
-   Reservable modules are updated.
-   Reservable paths are updated.

**Note:** All mandatory fields must be entered. The auto search capability is not triggered on the advanced search page if the mandatory fields are not filled in.

</td></tr><tr><td>

auto\_refresh\_search\_rsv\_data

</td><td>

Auto Refresh time interval\(in mins\) for showing reservables information while making a reservation. No auto refresh if set to 0 or negative number. Default value is 2 mins. Every 2 minutes \(depending on the property value that you have provided in the sn\_wsd\_rsv.auto\_refresh\_search\_rsv\_data\), the search results are refreshed. If results on the search page are outdated, the following message is shown along with a clickable referesh link, "The results you are viewing may be outdated. Please refresh to ensure you see the latest updates. Refresh the results."

</td></tr><tr><td>

\[sn\_wsd\_rsv.search\_limit\]

</td><td>

This property enables you to specify the number of workplace items to be displayed in the search result. If an employee applies any filter or sorting on the search results, the first 100 workplace items that match the criteria are displayed at a time. 100 is the default value. The value specified in this property is used only if there is no value specified in the **Search limit** field of a reservable module.-   Type: Integer
-   Default value: **100**

</td></tr><tr><td>

sn\_wsd\_rsv.time\_before\_check\_in\_out\_reminder

</td><td>

This property enables you to configure when to send a notification email as a reminder to employees to check in or check out a reservation. The value must be set in minutes.-   Type: Integer
-   Default value: **30**

</td></tr><tr><td>

sn\_wsd\_rsv.day\_start

</td><td>

This property enables you to specify the start time of an all day reservation. The value must be set in 24-hour format.-   Type: String
-   Default value: **09:00**

</td></tr><tr><td>

sn\_wsd\_rsv.day\_end

</td><td>

This property enables you to specify the end time of an all-day reservation. The value must be set in 24-hour format.-   Type: String
-   Default value: **17:00**

</td></tr><tr><td>

sn\_wsd\_rsv.is\_blocker\_mandatory

</td><td>

This property enables you to specify if the blocker reservations are mandatory. The blocker reservations are created for preparation and clean-up activities if an extra service is requested along with the reservation. If you enable this property, and if the blocker reservations collide with another reservation, then the extra service will not be requested. The employee who made the reservation with these extra service, can view the message about the rejected service on the Reservation summary page. **Note:** If an extra service is requested for a workplace location that requires approval, the blocker reservations are sent for approval along with the actual reservation.

 -   Type: true/false
-   Default value: **false**

</td></tr><tr><td>

sn\_wsd\_rsv.blocker\_user

</td><td>

This property enables you to specify the user who is used to create the blocker reservations.-   Type: String
-   Default value: **9b21b32ddb88b01097acc900399619d8**

</td></tr><tr><td>

sn\_wsd\_rsv.cancel\_unconfirmed\_reservations

</td><td>

This property enables you to specify after how many minutes should a reservation be canceled if there is no confirmation from the calendar provider.-   Type: Integer
-   Default value: **360**

</td></tr><tr><td>

sn\_wsd\_rsv.time\_when\_reservation\_cancelled\_without\_check\_in

</td><td>

This property enables you to specify after how many minutes should a reservation be canceled if it is not checked in. Ensure that the you have enabled the **Cancel reservations exceeding check-in time** option in the reservable module on which you want to apply this action. -   Type: Integer
-   Default value: **30**

</td></tr><tr><td>

sn\_wsd\_rsv.default\_quick\_reserve\_reservable\_module

</td><td>

This property enables you to specify the default reservable module that must be available on the Now Mobile app to employees for quick reservation. Specify the sys\_id of the reservable module that supports quick reservation.-   Type: String
-   Default value: empty

</td></tr><tr><td>

sn\_wsd\_rsv.meeting\_provider

</td><td>

This property enables you to set the virtual meeting providers to generate a meeting link.-   Type: choice list
-   Default value: none

</td></tr><tr><td>

sn\_wsd\_rsv.recording\_buffer\_time

</td><td>

This property enables you to set the time in minutes by when ta meeting recording must be retrieved.-   Type: integer
-   Default value: 30

</td></tr><tr><td>

sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY

</td><td>

This property enables you to set privacy on location and also specify what type of privacy you want to set.-   Type: choice list
-   Default value: none

</td></tr><tr><td>

sn\_wsd\_rsv.enable\_recurring\_score

</td><td>

This property enables you to display recurring availability within the series of a workplace location when an employee searches for workplace to make a recurring reservation.-   Type: true/false
-   Default value: false

</td></tr><tr><td>

sn\_wsd\_rsv.lead\_time\_info\_message\_for\_limited\_services

</td><td>

This property enabled displays a message ''Only items that can be prepared on time are available''.This message is displayed only for the special user sn\_wsd\_case.bypass\_services\_limitation and not for regular employees.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](components-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](proximity-calculation-for-browse-near-person.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Mobile push notifications for workplace reservations](reservation-push-notifications.md)

[Location privacy settings and impact](location-privacy-settings-and-impact.md)

[Additional details record producer - Mapping Variable types and limitations](custom-fields-record-producer-mapping-variable-type-conditions.md)

