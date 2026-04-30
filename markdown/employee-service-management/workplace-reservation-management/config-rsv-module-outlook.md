---
title: Configure Reservable Module for Microsoft Outlook
description: Configure Reservable Module settings for Microsoft Outlook in Workplace Reservation Management version 3.0.2. Employees can create a meeting or an event in the Microsoft Outlook calendar, and reserve a space using the Workplace Reservation Management manifest add-in file.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 22
breadcrumb: [Manage Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Reservable Module for Microsoft Outlook

Configure Reservable Module settings for Microsoft Outlook in Workplace Reservation Management version 3.0.2. Employees can create a meeting or an event in the Microsoft Outlook calendar, and reserve a space using the Workplace Reservation Management manifest add-in file.

## Before you begin

Configure the Reservable module for Microsoft Outlook Add-in, and configure it with a Reservable Module.

**Note:** Employees assigned to one or more Reservable Modules should have the sn\_wsd.workplace\_user role.

**Note:** If you’re updating or migrating from Microsoft Outlook Add-in 1.12.2 version or earlier to Workplace Reservation Management 3.0.2, the **sn\_wsd\_msaddin.default\_reservable\_module** is updated automatically. The sys\_id of the default Reservable Module in this property is updated to the latest version of the Outlook Add-in Manifest file. After installing Workplace Reservation Management 3.0, employees can select the updated Reservable Module \(for example, Desks\). They can also opt to use any other Reservable Module assigned to them.

Install and configure the following:

-   Workplace Reservation Management
-   Workplace Core
-   Workplace Calendar Synchronization
-   Workplace Indoor Mapping
-   Workplace Case Management
-   Workplace Space Management

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservable Module**.

2.  Select a Reservable Module.

    For example: Meeting rooms

3.  The Reservable Module form opens.

    On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Name for the reservable module. For example, for meeting rooms, the name should be categorical like meeting rooms or rooms.|
    |Title|Title for the reservable module. The title is displayed on headline on reservation page on portal. For example, meeting rooms.|
    |Inline Title|Inline Title for the reservable module. The title is displayed inline with a descriptive text on the reservation Portal. For example, meeting rooms.|
    |Order|Order in which the reservable module must appear on the Reservation portal. For example, 100|
    |Active|Option to enable the reservable module available for reservation. Select the check box to enable it.|
    |Active from|Date from when the reservable module must be active and available for reservation.|

    Administrators can configure the following form options:

    -   **Reservable Table Configuration**

        Option to configure buildings and spaces for a location.

    -   **Reservable Module Configuration**

        Option to select the Outlook Add-in configurations for multi-building, neighborhood reservations, and so on.

    -   **Reservable Widget Configuration**

        Option to configure invitees, reservation subject, reservation cancel notes, additional details record producer, display reservation on behalf of, and so on.

    For more information, see [Configure a reservable module](config-reservable-module.md).

4.  Select the **Reservable Table Configuration** tab to configure locations for reservation.

    ![Reservable Table Configuration form.](../image/Reservable-module-table.png)

    On the form, fill in the fields.

<table id="table_zkf_5wr_wfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Selection type

</td><td>

Type of selection to display in the search results when employees search. Select one of the following options:-   **Specific unit**: The search result displays every workplace item.
-   **Container**: The search result displays the parent or container of the workplace items. If you select **Container**, the search results are displayed in groups with a defined quantity available for reservation. Employees can select a container to reserve and any available space from the container is assigned for reservation.


</td></tr><tr><td>

Reservable type

</td><td>

Type of the reservable item. For example, Location

</td></tr><tr><td>

Reservable table

</td><td>

Option to select the workplace items for reservation from a table. The table contains the reservable workplace spaces or items.**Note:** If you have selected **Location** as **Reservable type**, you should use only the Space \[sn\_wsd\_core\_space\] table and its extended tables.

</td></tr><tr><td>

Reservable filter

</td><td>

Option to apply filter conditions on the reservable items in the Reservable table. The reservable items are displayed on the application based on the given conditions. -   To add a condition, select **Add Filter Condition**.
-   To add an OR condition, select **Add "OR" Clause**.

For example: Active = True &amp; Is reservable = True &amp; Space type = Desk &amp; Building.Isreservable = True &amp; Floor.is reservable= true

 **Note:** If you’re adding a filter on a location, verify that the **Active** and **Is reservable** fields are set to **True**. If these values aren’t selected, inactive items or non- reservable items are displayed while making a reservation.

</td></tr><tr><td>

**Area \(Container\) selection** section

</td><td>

Enter the required field values.

</td></tr><tr><td>

Reservable container field

</td><td>

Specify on what basis that the reservable module should be grouped. The field appears only if you have selected **Container** value in the **Selection type** field. The field is automatically set to **Area**. For example, when the field is set to **Area**, the reservation search results appear as groups based on areas.

</td></tr><tr><td>

Reservable quantity field

</td><td>

Option to specify the reservable quantity for workplace items. The **Reservable Quantity** field determines the number of times a location or reservable items can be booked within a specific reservation time period. This setting provides flexibility in configuring space reservations without out the need to create individual space records for reservation. For example, if you select **Reservable Quantity**, the container can be reserved as many times as the combined reservable quantity values of all spaces within that container. The reservable quantity depends on the number of spaces provided in the Capacity column of the Workplace Core Space table.

</td></tr></tbody>
</table>5.  Select the **Reservable Module Configuration** tab.

    **Note:** Recurring, shift-based, and group reservations aren’t supported for Microsoft Outlook add-in reservations.

    ![Select Outlook Add-in the Reservable Module Configuration tab.](../image/outlook-rsv-module-config-tab-addin.png)

    On the form, fill in the fields.

<table id="table_imf_bxr_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available in

</td><td>

Select **Outlook Add-in** to enable Microsoft Outlook Add-in reservations. For more information, see [Create a reservation in Microsoft Outlook add-in](outlook-create-rsv.md)**Note:** If you’re updating or migrating from Microsoft Outlook Add-in 1.12.2 or earlier, the default Reservable Module's sys\_id in the **sn\_wsd\_msaddin.default\_reservable\_module** is updated to Workplace Reservation Management 3.0.2. Employees can continue using the default Reservable Module after migrating. They can also use a different Reservable Module assigned to them. For more information, see [Manage Workplace Reservations for Microsoft Outlook Add-in](../concept/manage-outlook-addin-rsv.md).

</td></tr><tr><td>

Require allocation check

</td><td>

Option to check if there’s an allocation mismatch between the workspace item and the logged-in user. This option appears only if you have Workplace Space Management installed.For workplace entities, the search results also display locations that are allocated to the parent entity.

</td></tr><tr><td>

Enable allocation duration check

</td><td>

Option to display spaces in the search results based on the start and end dates of the allocation. This field appears only when the **Require allocation check** field is selected.For recurring reservations, the allocation duration is only checked for the first occurrence.

**Note:**

-   In Workplace Space Management version 1.12.0, spaces that have the overlapping allocation and reservation time-frames are qualified for the reservation.
-   From Workplace Space Management version 1.13.0, spaces that don’t have overlapping allocation and reservation time-frames are considered unallocated spaces and are qualified for reservation.


</td></tr><tr><td>

Enable restricted neighborhood rules

</td><td>

Option to apply neighborhood restrictions on the spaces while displaying search results. The search results are displayed based on the restrictions applied on spaces. Restricted users can’t view spaces that they aren’t enabled to access. The restricted neighborhoods are automatically filtered out if the logged-in user is restricted.

</td></tr><tr><td>

Enable browse by area

</td><td>

Option to enable employees to search for a workplace based on area.

</td></tr><tr><td>

Enable browse by neighborhood

</td><td>

Reservation admin can indicate if neighborhood spaces are available for reservations. Employees can search in the context of a neighborhood and only the available spaces in a neighborhood are displayed for space reservation. For more information, see [Create neighborhood reservations](create-neighborhood-reservations.md).This option is also available on the Now Mobile app.

</td></tr><tr><td>

Enable browse favorites on Native Mobile

</td><td>

Option to enable employees to search from their favorite spaces on the Now Mobile app.**Note:** This option appears only if you have Employee Center 25.0.0 and for employees who have Now Mobile app installed. Verify that the Mobile Employee Service Portal is enabled.

 **Note:** This option is available only for the Now Mobile app app.

</td></tr><tr><td>

Override approval policy

</td><td>

Option to specify how to implement the approval policy. Choices are as follows:-   **No override**: The approval policy is implemented as set in the **Requires approval** field of a workplace space or room.
-   **Always require approval**: The approval policy is required regardless of what is set in the **Requires approval** field of a workplace space or room.
-   **Never require approval**: The approval policy is removed irrespective of what is set in the **Requires approval** field of a workplace space or room.


</td></tr><tr><td>

Apply to shift

</td><td>

Option to enable shift-based reservation on the module.**Note:** Shift-based reservations aren’t supported for Microsoft Outlook Add-in reservations.

</td></tr><tr><td>

Enable floor-based search

</td><td>

Option to enable employees to search for a workplace based on floor using the **Browse All**.

</td></tr><tr><td>

Time before employee can check-in

</td><td>

Option to specify the time before an employee can check in their reservation before it starts.

</td></tr><tr><td>

Override check-in policy

</td><td>

Option to specify how to implement the reservation check-in policy. Choices are as follows:-   **No override**: The check-in policy is implemented as set in the **Requires check-in** field of a workplace space or room.
-   **Always require check-in**: The check-in policy is required regardless of what is set in the **Requires check-in** field of a workplace space or room.
-   **Never require check-in**: The check-in policy is removed irrespective of what is set in the **Requires check-in** field of a workplace space or room.


</td></tr><tr><td>

Cancel reservations exceeding check-in time

</td><td>

Option to cancel a reservation if an employee doesn’t check in within the specified time.

</td></tr><tr><td>

Enable group reservation

</td><td>

Option to enable group reservation for a selected Reservable Module Configuration. For example, **Desks**.**Note:** If the **Allow invitees** check box option is selected in the Reservation Widget Configuration, you can’t make a group reservation. The Reservation Widget Configuration tab is available in the Reservable Module.

</td></tr><tr><td>

Enable employees to make spaces as private

</td><td>

Option to enable employees to make the space details private when they make a reservation. When an employee is creating a reservation, the option **Make space details private** is displayed only if the employees are allowed to override their privacy preference for the selected space. Whether an employee can override privacy or not depends on the location privacy setup.

</td></tr><tr><td>

Enable ical generation

</td><td>

Option to enable user to generate an icalendar. **Note:** A user can’t download an iCalendar for spaces and reservations that already synchronizes with their calendar provider.

</td></tr><tr><td>

Default reservation path when editing a reservation

</td><td>

Option to set the context \(Reservation Path\) when editing a reservation. This option is also available on the Now Mobile app. The reservation paths define the available search criteria. Select any of the following options from the drop-down list:

 -   **Based on reservation**:

While editing a reservation, employees can search in the context \(Reservation Path\) used while creating a reservation.

For example: **Browse all**,**Browse an area**, **Browse by neighborhood**.

-   **Browse all**:

When editing a reservation, the context \(path\) is defaulted to **Browse all**. Employees can change the selected space or date and time of the reservation.

 For more information, see [Create a reservation](create-reservation-request-1.md).

 **Note:** This option isn’t available on the Now Mobile app.

</td></tr><tr><td>

Virtual meeting provider

</td><td>

Select a virtual meeting provider to enable employees to create a virtual meeting link. If an employee selects the **Add a virtual meeting link** option, a virtual meeting link is automatically generated by the virtual meeting provider.

</td></tr><tr><td>

Allow Multiple Building Reservations

</td><td>

Option to add multiple buildings and select spaces from the buildings in a single reservation. The buildings can belong to different regions or locations and can be from different time zones. **Note:** Adding multiple buildings to a reservation is available only on the Workplace Service Portal. Recurring reservations aren’t supported for multi-building reservations. For more information, see [Create multi-building reservations](create-multi-building-reservation.md).

</td></tr><tr><td>

Max days in future

</td><td>

Option to specify the maximum number of the days in the future up to which the reservable module can be reserved. For example, if you set the max number of days in future to **90**, employees can make future reservations on this module only up to 90 days in advance. If this option is enabled, employees can’t select a date beyond the specified value in **Max days in future** while making a reservation. For more information, see [Create a reservation](create-reservation-request-1.md).

On Now Mobile app, if you try to select a date too far in the future than what is specified in the **Max days in future**, no results are returned.

**Note:** **Max days in future** field indicates that the user can’t make a reservation beyond the number of days configured as the **Max days in future** value for any reservation. **Max days in future** is a reservation property and **Max number of occurrences** is a recurring reservation property. **Max days in future** value takes priority when both these options are used for the reservation.

For example, if the **Max days in future** is 90 days, then the number of occurrences in the recurring reservation can’t exceed 90 days even if the employee has initially configured the value for Max number of occurrences as 180 days in the Reservable module.

</td></tr><tr><td>

Max number of occurrences

</td><td>

Option to specify the maximum number of occurrences for recurring reservation that can be made on the reservable module. The default value is 180. This option depends on the **Allow recurring reservations** check box field. If **Allow recurring reservations** isn’t selected, the **Max number of occurrences** field is inactive.

</td></tr><tr><td>

Min duration

</td><td>

Option to specify the minimum reservation duration of the reservable module.

</td></tr><tr><td>

Max duration

</td><td>

Option to specify the maximum reservation duration of the Reservable Module.

</td></tr><tr><td>

Max days for multi-day

</td><td>

Option to make a multi-day reservation. Employees can reserve an available space covering or spanning multiple days. For example, 5 days or more. For more information, see [Create a multi-day reservation](create-multi-day-reservation.md).Default value for this Reservable Module property is 1. To make a single day reservation, set the value to 1. Value 0 \(zero\) isn’t enabled.

When the **Max days for multi-day** value is more than 1, the **All day** option is inactive on the Reservation portal while making a reservation.

**Note:** The number of days for this property must not exceed the **Max days in future** value on the Reservable Module.

</td></tr><tr><td>

Enable browse near a person

</td><td>

Option to enable employees to search for spaces near a person. When an employee searches for a space near a person, the available spaces located on the user's floor are displayed. The display criteria are also based on the nearby area of the space or tags assigned to the spaces.**Note:** If the option is enabled, the search limit criteria are not applicable.

</td></tr><tr><td>

Max number of days for browse near a person

</td><td>

Option to specify the number of days employees can reserve a space near a colleague. Admins can configure the maximum number of days an employee would like to reserve a space near a colleague using this property.Default value is 7. Administrators can change this value to more than 7 days and enable employees to select the max number of days they would like to book a seat near a team member or a colleague. For more information, see [Create a reservation](create-reservation-request-1.md).

**Note:** This field is displayed only when the **Enable browse near a person** Reservable module property is enabled on the Reservable Module.

The number of days provided for this property can’t be 0 or a negative number \(for example, -10\). The number of days for this property must not exceed the **Max days in future** value on the Reservable Module.

</td></tr><tr><td>

Allow all day reservation

</td><td>

Option to enable employees to reserve a workplace item of the module for an entire day. If the check box is cleared, the Require all day reservation field is inactive.

 Note: If the Max days for multi-day Reservable Module value is set to more than 1 day, the All day option is inactive on the Reservation portal. If the Max days for multi-day value is set to 1, then employees can only make a single day or all day reservation.

 For more information, see the Max days for multi-day property description.

 For example: Default value 9 AM to 5 PM.

</td></tr><tr><td>

All day

</td><td>

Option to enable manage **All day** reservation option on the reservation portal. Select one of the following options:

-   Disabled: The **All day** option is disabled and not available for employees while making a reservation. The **All day** option isn’t displayed on the Reservation portal.

-   Enabled: The **All day** option is available to the employees on the reservation portal. They can opt to select the option when required.

-   Default: The **All day** option is available and selected by default. The employees can opt not to select the check box or change the timings if necessary.

-   Required: The **All day** check box is selected and can’t be changed on the reservation portal. The **All day** field is set as required.

</td></tr><tr><td>

Max days in future

</td><td>

Option to specify the maximum number of the days in the future up to which the reservable module can be reserved. For example, if the Max number of days in future is set to 90, employees can make future reservations only up to 90 days in advance.

 If this option is enabled, users can’t select a date beyond the specified value in Max days in future while making a reservation. For more information, see [Create a reservation](create-reservation-request-1.md).

 **Note:** **Max days in future** value indicates that the user can’t make a reservation beyond the number of days configured in this option. Max days in future is a reservation property and Max number of occurrences is a recurring reservation property. Max days in future value takes priority when both these options are used in a reservation.

 For example, if the **Max days in future** is 90 days, the number of occurrences in the recurring reservation can’t exceed 90 days even when an employee has initially configured the value for Max number of occurrences as 180 days in the Reservable module.

</td></tr><tr><td>

Max number of occurrences

</td><td>

Option to specify the maximum number of occurrences for recurring reservation that can be made on the reservable module. The default value is 180. This option depends on the Allow recurring reservations check box field. When **Allow recurring reservations** check box isn’t selected, the **Max number of occurrences** option is inactive.

</td></tr><tr><td>

Min duration

</td><td>

Option to specify the minimum reservation duration of the reservable module.

</td></tr><tr><td>

Max duration

</td><td>

Option to specify the maximum reservation duration of the reservable module.

</td></tr><tr><td>

Max days for multi-day

</td><td>

Option to make a multi-day reservation. Employees can reserve an available space covering or spanning multiple days. For example, 5 days or more. For more information, [Create a multi-day reservation](create-multi-day-reservation.md).

 Default value for this Reservable Module property is 1. To make a single day reservation, set the value to 1. Empty value or zero isn’t enabled.

 When the Max days for multi-day value is more than 1, the **All day** option is inactive on the Reservation portal while making a reservation.

 **Note:** The number of days provided for this property must not exceed the Max days in future value on the Reservable Module.

</td></tr><tr><td>

Enable browse near a person

</td><td>

Option to enable users to search for spaces near a colleague or team member for better collaboration. When employees search for a space near a team member, available spaces near the team member are displayed.

 Select the check box to enable this option.

 **Note:** The search limit property value isn’t enabled if this option is enabled.

</td></tr><tr><td>

Max number of days for browse near a person

</td><td>

Option to specify the number of days employees can reserve a space near a colleague. Administrators can configure the maximum number of days an employee would like to reserve a space near a colleague using this property.

 Default value is 7. Administrators can change this value to more than 7 days and enable employees to select the max number of days to book a seat near a team member or a colleague. For more information, see [Create a reservation](create-reservation-request-1.md).

 **Note:** This field is displayed only when the **Enable browse near a person** Reservable module property is enabled on the Reservable Module.

 The number of days provided for this property can’t be empty, zero, or a negative integer \(for example, -10\). The number of days provided for this property must not exceed the **Max days in future** value.

</td></tr><tr><td>

Enable facet filter

</td><td>

Option to enable facet filter on the workplace items. If the select this option, the filter options are displayed based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.

</td></tr><tr><td>

Search limit

</td><td>

Option to specify the maximum limit of search results when an employee searches for a workplace location.

</td></tr></tbody>
</table>6.  Select the **Reservation Widget Configuration** tab.

    ![Reservation Widget Configuration form.](../image/reservable-widget-configuration.png)

    Fill in the form information:

<table id="table_rkb_rxr_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires subject

</td><td>

Option to make a reservation subject as required before making a reservation. If this check box is selected, employees should add a reservation subject before submitting their reservation.

</td></tr><tr><td>

Require cancel notes

</td><td>

Option to make a cancellation note required before making a cancellation.

</td></tr><tr><td>

Warn employee for duplicate reservation

</td><td>

Option to warn employees if a reservation exists for the selected space type module during the specified date and time for that employee. The warning is displayed based on the date and time specified in the search criteria.

</td></tr><tr><td>

Warn employee about presence exception

</td><td>

Option to warn employees if their presence is set to remote on the date of the reservation. The warning is displayed based on the [presence routine](../../workplace-concierge/concept/explore-workplace-concierge.md#section_nz5_lxh_tzb) of the employee. This option is available if [Workplace Concierge](../../workplace-concierge/concept/workplace-concierge-feat.md) is installed.

</td></tr><tr><td>

Allow invitees

</td><td>

Option to enable employees to invite attendees to their reservation. Employees can invite co-workers and also external visitors.-   If the **Allow invitees** check box is selected, the **Display number of attendees** and **Enable Group Reservations** check box options are cleared and not selected by default.
-   If **Display number of attendees** is selected, the **Allow invitees** check box selection is unselected by default.

**Note:** You can’t make Group reservations for Microsoft Outlook Add-in.

**Note:** For Microsoft Outlook Add-in reservations, you should set the**sn\_wsd\_rsv.display\_invitees\_on\_outlook** value to true. If the **Allow invitees** option is selected and the **sn\_wsd\_rsv.display\_invitees\_on\_outlook** is set to true,employees can see the option to select invitees when making a reservation using Microsoft Outlook Add-in.

For more information, see [Properties installed with Workplace Reservation Management](../reference/properties-installed-with-wsd-reservation-mgmt.md).

If **Allow invitees** is set to false, and **sn\_wsd\_rsv.display\_invitees\_on\_outlook** property is set to true, then the property value is given priority and employees are allowed to add invitees to a reservation. If **Allow invitees** is true, and **sn\_wsd\_rsv.display\_invitees\_on\_outlook** is set to false, employees can’t add invitees to a reservation.

</td></tr><tr><td>

Display number of attendees

</td><td>

Option to enable employees to specify the number of attendees while making a reservation. If the option isn’t selected, then the number of attendees is automatically set to **1**. **Note:** If the **Allow invitees** check box is selected, the **Display number of attendees** becomes inactive and read only. The **Enable Group Reservations** check box in the **Reservable Module Configuration** tab also becomes read only and inactive.

You can’t make group reservations for Microsoft Outlook Add-in.

</td></tr><tr><td>

Display on behalf of

</td><td>

Option to enable employees to specify on whose behalf they’re making a reservation. The option is enabled by default. An error is displayed if the option is inactive.

</td></tr><tr><td>

Display sensitivity

</td><td>

Option to enable employees to set the sensitivity of the reservation. They can set a reservation to **Normal** or **Private**. If the option isn’t selected, the sensitivity is set to **Normal** and the subject will be visible to others.

</td></tr><tr><td>

Allow reservation message

</td><td>

Option to add notes to a meeting and attach images while making a reservation. The notes and images can be shared with the meeting invitees.**Note:** When calendar synchronization is enabled for a space, the message or notes are added to the body of the reservation.

For Now Mobile app, the message is displayed on the summary page but employees can’t add or edit a message.

For more information, see [Create a reservation](create-reservation-request-1.md).

.

</td></tr><tr><td>

Additional details record producer

</td><td>

Option to link to the record producer that you have configured with additional fields. You can display additional fields on the reservation form. For more information, refer to [Configure reservable module with additional details](configure-reservable-module-with-custom-fields.md).

</td></tr><tr><td>

Show as

</td><td>

Option to specify what status of the reservation that is shown on the employee's calendar when a reservation is synchronized. This field appears only if Workplace Calendar synchronization is installed. -   **Busy**: The reservation is displayed in the Employee's calendar with a Busy status. The employee's calendar is blocked during the reservation duration.
-   **Free**: The reservation is displayed in the Employee's calendar with a Free status. The employee's calendar won’t be blocked during the reservation duration.
 **Note:** For the **Show as** feature to work correctly, you must have the following versions of the Microsoft Outlook connections:

-   For Microsoft, you must have Microsoft Exchange Online spoke version 3.2.4.
-   For Google Calendar, you must have the Google Calendar version 2.3.1.


</td></tr></tbody>
</table>
