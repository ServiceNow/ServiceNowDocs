---
title: Components installed with Workplace Reservation Management
description: Several types of components are installed with activation of the Workplace Reservation Management application, including tables, user roles, and business rules.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Workplace Reservation Management references, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Reservation Management

Several types of components are installed with activation of the Workplace Reservation Management application, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this application.

## Roles installed with Workplace Reservation Management

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

WSD Core Admin\[sn\_wsd\_core.admin\]

</td><td>

Complete access to Workplace Service Delivery applications.

</td><td>

sn\_wsd\_rsv.admin

</td></tr><tr><td>

WSD Admin\[sn\_wsd\_rsv.admin\]

</td><td>

-   Manage Standard services and the location to which they are assigned.
-   Add standard services.
-   Add flexible services
-   Add reservable purposes.
-   Assign archiving rule.
-   Create and assign time slots to a reservable module.

</td><td>

-   sn\_wsd\_rsv.manager
-   sn\_wsd\_rsv.dispatcher
-   sn\_wsd\_rsv.staff
-   sn\_wsd\_core.workplace\_user
-   sn\_wsd\_rsv.reservation\_planner

</td></tr><tr><td>

WSD Manager\[sn\_wsd\_rsv.manager\]

</td><td>

-   View all reservations.
-   View and generate reports.
-   Manage reservations.

</td><td>

-   sn\_wsd\_rsv.dispatcher
-   sn\_wsd\_rsv.staff
-   sn\_wsd\_core.workplace\_user
-   sn\_wsd\_rsv.reservation\_planner

</td></tr><tr><td>

WSD Dispatcher\[sn\_wsd\_rsv.dispatcher\]

</td><td>

View all reservations.

</td><td>

-   sn\_wsd\_rsv.staff
-   sn\_wsd\_core.workplace\_user

</td></tr><tr><td>

WSD Staff\[sn\_wsd\_rsv.staff\]

</td><td>

View all reservations.

</td><td>

sn\_wsd\_core.workplace\_user

</td></tr><tr><td>

Workplace user\[sn\_wsd\_core.workplace\_user\]

</td><td>

-   Create room or desk reservations from the Service Portal for self or on behalf of someone.
-   View reservations created by them.
-   View reservations created on behalf of themselves or someone else.
-   Manage \(edit and cancel\) reservations created by them.
-   View private subject of their reservations or reservation created for them.
-   View reservable items.
-   View services.

</td><td>

None

</td></tr><tr><td>

Reservation planner\[sn\_wsd\_rsv.reservation\_planner\]

</td><td>

Plan reservations in Workplace Central Event planner

</td><td>

-   sn\_wsd\_rsv.dispatcher
-   sn\_wsd\_rsv.reservation\_viewer
-   sn\_wsd\_case.bypass\_services\_limitation

Reservation planner and space planners are allowed to ignore or bypass the Reservable module configuration settings.

For more information, see [Allow Event planners to handle reservations with more flexibility](../../workplace-central/concept/event-planner-bypass-validation-rule-overview.md).

-   sn\_wsd\_rsv.bypass\_module\_validation

</td></tr><tr><td>

Reservation viewer\[sn\_wsd\_rsv.reservation\_viewer\]

</td><td>

View reservations inWorkplace Central Event planner.

</td><td>

-   sn\_wsd\_core.workplace\_user
-   sn\_wsd\_central.workplace\_analytics\_user

</td></tr></tbody>
</table>## Tables installed with Workplace Reservation Management

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Space Suggestions\[sn\_wsd\_core\_user\_space\_suggestions\]

</td><td>

Retrieves user preferred space suggestions for employees having a workplace user profile. Make sure that Workplace Concierge is installed. For more information, see [User Space Suggestions](../../workplace-concierge/task/userspace-suggestions.md).

</td></tr><tr><td>

Space Suggestion Configuration\[sn\_wsd\_core\_space\_suggestion\_configuration\]

</td><td>

Retreives user preferrences from the space suggestion configuration table. Make sure that Workplace Concierge is installed. Admin can specify the configuration and the space logic that needs to be considered while suggesting workplace locations, preferred collaborators, and workplace services to an employee. For more information, see [Space suggestion Configuration](../../workplace-concierge/task/space-suggestion-configuration.md).**Note:** Make sure only one record exist for each preference type.

</td></tr><tr><td>

Reservable Module\[sn\_wsd\_rsv\_reservable\_module\]

</td><td>

Extends the Application File table. Stores information about items that can be reserved.

</td></tr><tr><td>

Workplace Reservation\[sn\_wsd\_rsv\_reservation\]

</td><td>

Extends the Reservation \[sn\_wsd\_core\_reservation\] table. Stores information about reservations.**Note:** A new column **Auto Conflict Resolution state** is added to this table for indicating auto resolution states:

1.  **In progress**: Process of resolving auto-conflicts is in progress.
2.  **Automaically resolved**: Application automatically resolves the conflicted reservations.
3.  **Not resolved**: Reservation events that the system could not resolve automatically.
4.  **Manually resolved**: Users need to manually resolve the recurring reservation conflicts.
5.  **Partially resolved**: Reservation conflicts which the system was not able resolve fully.
6.  **All resolved**: All recurring reservations are successfully resolved.

</td></tr><tr><td>

Standard Service\[sn\_wsd\_rsv\_standard\_service\]

</td><td>

Stores information about standard services.

</td></tr><tr><td>

Workplace rooms\[sn\_wsd\_core\_room\_list\]

</td><td>

Extends the Space \[sn\_wsd\_core\_space\] table. It holds the reservable items of a room that are available to reserve.

</td></tr><tr><td>

Reservable purpose\[sn\_wsd\_rsv\_reservable\_purpose\]

</td><td>

Stores information about reservable purposes added to Workplace spaces and Workplace Rooms.

</td></tr><tr><td>

Extra service \[sn\_wsd\_rsv\_extra\_service\]

</td><td>

Stores information about extra services requested by employee while making a reservation.

</td></tr><tr><td>

Reservable Time Slot \[sn\_wsd\_rsv\_time\_slot\_list\]

</td><td>

Stores information about the time slots.

</td></tr><tr><td>

Reservable View\[sn\_wsd\_rsv\_reservable\_view\]

</td><td>

Stores information about the reservable views.

</td></tr><tr><td>

Reservation path\[sn\_wsd\_rsv\_reservation\_path\]

</td><td>

Stores information about all the reservation paths.

</td></tr><tr><td>

Reservable Module View Configurations\[sn\_wsd\_rsv\_m2m\_reservable\_module\_view\_configuration\]

</td><td>

Stores informations about the views that are displayed on the search page and their order.

</td></tr><tr><td>

Reservation recording\[sn\_wsd\_rsv\_reservation\_recording\]

</td><td>

Store information about all the reservation recordings.**Note:** If **WSD: Archive old reservations** archival rule is applied, then Reservation recording\[**sn\_wsd\_rsv\_reservation\_recording**\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Layout\[sn\_wsd\_rsv\_layout\]

</td><td>

Stores information about all the reservation layouts.

</td></tr><tr><td>

Location Layout\[sn\_wsd\_rsv\_m2m\_location\_layout\]

</td><td>

Stores information about the layouts if a location such as carrier, round and more.

</td></tr><tr><td>

Reservable Module Workplace Location\[sn\_wsd\_rsv\_m2m\_reservable\_module\_workplace\_location\]

</td><td>

Stores information about all the workplace locations assigned to a reservable module.

</td></tr><tr><td>

Virtual Meeting Provider\[sn\_wsd\_rsv\_virtual\_meeting\_provider\]

</td><td>

Stores information about all the virtual meeting providers configured in the application.

</td></tr><tr><td>

Reservation Invitee\[sn\_wsd\_rsv\_m2m\_reservation\_invitee\]

</td><td>

Stores information about all the reservation invitees.**Note:** If **WSD: Archive old reservations** archival rule is applied then Reservation invitee\[sn\_wsd\_rsv\_m2m\_reservation\_invitee\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Location Standard Service\[sn\_wsd\_rsv\_m2m\_location\_standard\_service\]

</td><td>

Stores information about all the standard services added to a workplace location.

</td></tr><tr><td>

Location Reservable Purpose\[sn\_wsd\_rsv\_m2m\_location\_reservable\_purpose\]

</td><td>

Stores information about reservable purposes added to workplace locations.

</td></tr><tr><td>

Reservable Module User Criteria\[sn\_wsd\_rsv\_m2m\_reservable\_module\_user\_criteria\]

</td><td>

Stores information about which users or groups have access to a reservable module.

</td></tr><tr><td>

Reservable Module Time Slot\[sn\_wsd\_rsv\_m2m\_reservable\_module\_time\_slot\]

</td><td>

Stores information about all the time slots of Quick Reservation Widget.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Properties installed with Workplace Reservation Management](properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](proximity-calculation-for-browse-near-person.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Mobile push notifications for workplace reservations](reservation-push-notifications.md)

[Location privacy settings and impact](location-privacy-settings-and-impact.md)

[Additional details record producer - Mapping Variable types and limitations](custom-fields-record-producer-mapping-variable-type-conditions.md)

