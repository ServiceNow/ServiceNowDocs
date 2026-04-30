---
title: Location privacy settings and impact
description: Set location privacy on workplace reservations and workplace profiles in your organization. Implement privacy throughout the organization or only on a building using the Workplace Service Delivery location privacy settings.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Reference, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Location privacy settings and impact

Set location privacy on workplace reservations and workplace profiles in your organization. Implement privacy throughout the organization or only on a building using the Workplace Service Delivery location privacy settings.

## System property settings

Using the Workplace Reservation Management system properties you can specify your location privacy preferences on workplace profiles and workplace reservations that belong to your organization.

You can set the location privacy using the following navigation:

-   **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Properties**
-   System Properties \[sys\_properties\] table. To access the table, enter sys\_properties.list in the navigation filter.

The following properties are provided in the application to implement location privacy:

-   **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY**: Enables you to set location privacy preference. You can apply privacy on workplace profiles and workplace reservations. The following options are provided:
    -   **No privacy**: Select this option if you don’t want to set any privacy. The property is set to **No privacy** by default.
    -   **Workplace profiles only**: Select this option to set privacy on workplace profiles.
    -   **Reservations only**: Select this option to set privacy on workplace reservations.
    -   **Reservations and workplace profiles**: Select this option to set privacy on both workplace profiles and workplace reservations.
-   **sn\_wsd\_core.OVERRIDE\_RESERVATION\_PRIVACY**: Enables you to let employees override the location privacy on a reservation. The property is set to **no** by default.
-   **sn\_wsd\_core.PRIVACY\_INFORM\_EMPLOYEE**: Enables you to inform employees when privacy is applied on a workplace profile or reserved spaces. The property is set to **false** by default.

## Building settings

If required, you can apply different location privacy settings on a building. That is, you can set privacy on workplace profiles or reservations made on that building. The privacy setup on the building won’t affect other locations of your organization.

When you enable location privacy on a building, the privacy is inherited by the locations and workplace profiles in that building. The privacy setup of the building is considered instead of the privacy setup made on an organization level using the system properties.

In a building record, specify your location privacy preferences in the following fields:

-   **Enable employee location privacy and preference**: Use this field to set your location privacy preference for the building. The following options are provided:
    -   **None**: Select this option if you don’t have any particular privacy preference on the building. When you set this option, the privacy preference that is set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered. The field is set to **None** by default.
    -   **No privacy**: Select this option if you don’t have any privacy requirement.
    -   **Workplace profiles only**: Select this option to set privacy on workplace profiles.
    -   **Reservations only**: Select this option to set privacy on workplace reservations.
    -   **Reservations and workplace profiles**: Select this option to set privacy on both workplace profiles and workplace reservations.
-   **Allow employees to override location privacy on reservations**: Use this field to specify if you want to let employees override the location privacy while reserving spaces that belong to this building. The field provides the following override options:
    -   **None**: Select this option if you don’t have any particular privacy requirement. When you set this option, the location privacy override preference that is set in the Workplace Reservation Management system property **sn\_wsd\_core.OVERRIDE\_RESERVATION\_PRIVACY** is considered. The field is set to **None** by default.
    -   **Yes**: Select this option if you want to let employees override the privacy preference that is configured for the location that they want to reserve.
    -   **No**: Select this option if you want to restrict employees from overriding the privacy preference that is set on the location that they want to reserve.

## Workplace profile setting

If required, set location privacy on a workplace profile directly. By default, the location privacy preference that is set on the building in which the workplace profile is located is considered. In case, the building doesn't have any location privacy preference, the preference set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered.

The **Enable employee location privacy** field provides the following options:

-   **None**: If you set this option, then the privacy setting made on the building where the workplace profile is assigned is considered. The field is set to **None** by default.
-   **Yes**: Select this option if you want to set privacy on the workplace profile.
-   **No**: Select this option if you don’t want to set privacy on the workplace profile.

To specify privacy on a workplace profile, refer to [Map designated workspaces to user profiles](../../workplace-service-delivery/task/map-employees-to-existing-workplace-locations-wsd.md). The location privacy is implemented as follows:

-   If set you set the field as **Yes**, then privacy is set on the workplace profile.
-   If you set the field as **No**, then the workplace profile isn't set as private. Even if the building to which the workplace profile is located has privacy enabled, the workplace profile will still remain private.

## Reservable module setting

Apart from the location privacy settings that you make in the system properties or on a building, the application also enables you to make a setting on the reservable module. You can enable employees to set the space details as private while making reserving a space that belongs to the reservable module. Use the **Enable employees to make spaces as private** option to specify your location preference. For more information, refer to [Configure a reservable module](../task/config-reservable-module.md).

The privacy override of a space while making a reservation, depends on the following:

-   If the **Enable employees to make spaces as private** is enabled on the reservable module and if location privacy override by employees is set to **Yes** in the privacy override setup, then the employees can override privacy in their reservation. The **Make space details private** option appears to the employees while making a reservation.
-   If either the **Enable employees to make spaces as private** is turned off on the reservable module or if the location privacy override by employees is set to **No** in the privacy override setup, then the employees can’t override privacy in their reservation. The **Make space details private** option doesn't appear to the employees while making a reservation.

## Location privacy processing

The location privacy is processed as follows:

-   Always, the privacy setup that is made in the Workplace Reservation Management system property is considered except in case a building or a workplace profile has its own privacy setup.
-   Similarly, the privacy override setup that is made in the Workplace Reservation Management system property is considered except in case a building or a workplace profile has its own privacy override setup.
-   **Workplace profile**:
    -   If a workplace profile has privacy setup, then that is considered.
    -   If a workplace profile has no privacy setup, then the privacy setup that is set on the building in which the workplace profile is located is considered. If the building has no privacy setup, then the privacy setup that is set in the Workplace Reservation Management system property is considered.
-   **Building**:
    -   If a building has privacy setup, then that setup is considered.
    -   If a building has no privacy setup, then the privacy setup made in the Workplace Reservation Management system property is considered.

## Privacy information

When a reservation is requested, to know more about privacy-related setting, open the list of reservations through one of the following:

-   Workplace Core: Navigate to **All** &gt; **Workplace Core** &gt; **Space Reservations** &gt; **All reservations**.
-   Workplace Reservation Management: Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **All Reservations**.

From the list view of the reservations, you can know the following:

-   Privacy setting by viewing the **Space details private** column of the reservation. The column displays if the privacy setting is set as **True** or **False**.
-   Privacy information, that is, from which source the privacy has been implemented, by viewing the **Privacy info** column. The column provides details of how the privacy has been set for the reservation in detail.

## Impact of location privacy

Depending on the location privacy preferences, the following areas are affected.

-   **Browse near a person**

    Based on the location privacy, the fields in the Reservation portal **Browse near a person** section is influenced as follows. The following scenarios are explained using examples:

    -   If either the workplace profile of Employee A or if the reserved space of Employee A is private, then when another employee - Employee B searches for this employee to reserve a space nearby, the details related to the reserved space do not appear.
    -   If the reservation is made by Employee B for Employee A, or if Employee B is invited to the reservation, or if the reservation is shared with Employee B, only then, the reservation details of Employee A's reserved space appears in the search results for Employee B.
-   **Schedule view**

    On the Reservation portaI, if a reservation is marked as private, the **Schedule view** of the space won’t show any employee-related details if there’s a reservation for a certain time.

    If a reservation is made by Employee B for Employee A, or if Employee B is invited to the reservation, or if the reservation is shared with Employee B, only then the employee-related details of Employee A will appear in the **Schedule view** for Employee B.

-   **Location directory**

    When an employee uses the Workplace Service Portal Location directory to search for a colleague or a space, depending on the privacy setting, the following happens:

    -   If the colleague for which an employee is searching for has their workplace profile set as private, then their location details aren’t displayed.
    -   If there’s an ongoing private reservation of Employee A on a workspace/desk Space 123, on then
        -   If Employee B searches for Employee A, then the reserved space, Space 123, won’t appear in the search. A **Private** tag is displayed on the search result card.
        -   If Employee B searches for Space 123, then the details of Employee A who reserved this space won’t be displayed in the search results. A **Private profile** tag is displayed on the search result card.
    -   If a reservation is made by Employee B for Employee A, or if Employee B is invited to the reservation, or if the reservation is shared with Employee B, only then, the employee-related details appear in the Location directory for Employee B.

-   **Workplace Service Delivery for Mobile**

    If Employee A's workplace profile is set as private or has an ongoing private reservation, then when an Employee B searches for Employee A, or tries to get directions, the details related to the Employee A's location aren’t displayed. Also, the **Get directions** option isn’t displayed to Employee B.

    If any reservation is made by Employee B for Employee A, or if Employee B is invited to a reservation made by Employee A, or if the reservation by Employee A is shared with Employee B, only then, the employee-related details appear to Employee B. The **Get directions** option is displayed to Employee B.

-   **Quick Reservation widget**

    If the **Enable employee location privacy and preference** is set to **Reservations only** or **Reservations and workplace profile** in the privacy setup, then the space that is suggested as best match has privacy enabled by default.

    The option **Mark space details private** is displayed only if the employees are allowed to override their privacy preference for the space. Whether an employee can override privacy or not depends on the location privacy setup.

-   **Workplace Reservations for Microsoft Outlook Add-in**

    In the add-in, the privacy of the spaces that are displayed in the search results depends on their privacy setup. The option **Mark all space details private** is displayed only if the employees are allowed to override their privacy preference for the selected space. Whether an employee can override privacy or not depends on the location privacy setup.

-   **Workplace Calendar Synchronization**

    If a reservation is made using the Reservable Sync Configuration, then the privacy is implemented on the reservation based on the privacy setup made on the building to which the space belongs.


**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](components-installed-with-wsd-reservation-mgmt.md)

[Properties installed with Workplace Reservation Management](properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](proximity-calculation-for-browse-near-person.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Mobile push notifications for workplace reservations](reservation-push-notifications.md)

[Additional details record producer - Mapping Variable types and limitations](custom-fields-record-producer-mapping-variable-type-conditions.md)

