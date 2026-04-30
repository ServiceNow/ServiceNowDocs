---
title: Configure a reservable module
description: Create a Reservable Module to add a group of similar reservable workplace items. These workplace items are displayed in a single category on the Reservation portal.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-05"
reading_time_minutes: 27
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a reservable module

Create a Reservable Module to add a group of similar reservable workplace items. These workplace items are displayed in a single category on the Reservation portal.

## Before you begin

**Warning:** Starting with Workplace Reservation Management version 2.1.2, to create or view approvers or performer criteria, navigate to **Workplace Core** &gt; **Administration** &gt; **Performer Criteria**.

-   After the upgrade, the Reservable module's **Require approval** option is changed to **Override approval policy**.

    Before the upgrade, if a reservable module has the **Require approval** option enabled, then, after the upgrade, it is migrated as **Always require approval** in the **Override approval policy** option. Otherwise, the **Override approval policy** is set to **Never require approval**.

-   For existing customers, the Reservable module's approval functionality that were configured earlier to approve reservations remain the same until a new approval definition is configured. After you configure a new approval definition, the approval process will run according to the upgrade.

    After the upgrade, disable the **WSD Reservation Approval Flow** in the **Flow designer**.


Ensure that you have the following details:

-   Workplace data for your organization.
-   Data of workspaces that can be marked as available.
-   Configure approvers/performer criteria

See [Create records for your workplace data](../../workplace-service-delivery/task/create-records-of-workplace-data-wsd.md) to add workplace data.

Role required: sn\_wsd\_rsv.admin

## About this task

A Reservable module groups similar types of workplace items. Employees can view these similar items in one category. For example, a room is a reservable module and it contains similar workplace items like meeting rooms, conference rooms, and other rooms.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the reservable module. For example, for meeting rooms, the name should be categorical like `Desks`, `Meeting rooms`, or `Rooms` and so on.|
    |Inline title|Title for the reservable module. The title is displayed inline with a descriptive text on the Workplace Service Portal.|
    |Order|Order in which the reservable module must appear on the Reservation portal.|
    |Active|Option to make the module available for reservation.|
    |Active from|Date from when the reservable module must be active and available for reservation.|
    |Image|Image of the reservable module.|

4.  Select the Reservable Table Configuration tab.

    On the form, fill in the fields.

    ![Reseravable Table Configuration form.](../image/Reservable-module-table.png)

<table id="table_zkf_5wr_wfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Selection type

</td><td>

Type of selection to display in the search results when employees searche. Select one of the following options:-   **Specific unit**: The search result displays every workplace item.
-   **Container**: The search result displays the parent or container of the workplace items. If you select **Container**, the search results are displayed in groups with a defined quantity available for reservation. Employees can select a container to reserve and any available space from the container is assigned for reservation.


</td></tr><tr><td>

Reservable type

</td><td>

Type of the reservable item.

</td></tr><tr><td>

Reservable table

</td><td>

Table that contains the reservable workplace items.**Note:** If you selected **Location** for the **Reservable type** field, then use only the Space \[sn\_wsd\_core\_space\] table and its extended tables.

</td></tr><tr><td>

Reservable filter

</td><td>

Filter conditions on the reservable items in the Reservable table. The reservable items are displayed on the application based on the given conditions. You can do the following:-   To add a condition, select **Add Filter Condition**.
-   To add an OR condition, select **Add "OR" Clause**.
 **Note:** If you are adding a filter on a location, ensure that the **Active** and **Is reservable** fields are set to **True**. If you do not, then inactive items that are not reservable will be displayed as reservable.

</td></tr><tr><td>

**Area \(Container\) selection** section

</td><td>

Specify the field details.

</td></tr><tr><td>

Reservable container field

</td><td>

Specify on what basis must the be grouped. The field appears only if you selected **Container** as the **Selecttion type**. The field is automatically set to **Area**. For example, when the field is set to **Area**, the reservation search results will appear as groups based on areas.

</td></tr><tr><td>

Reservable quantity field

</td><td>

Reservable quantity for workplace spaces. The **Reservable Quantity** field determines the number of times a container can be booked within a specific reservation time period. This setting provides with flexibility in setting up space reservations without out the need to create individual space records for reservation. For example, if you select **Reservable Quantity**, the container can be reserved as many times as the combined reservable quantity values of all spaces within that container allow. The reservable quantity depends on the number of spaces provided in the Capacity column of the Workplace Core Space table.

</td></tr></tbody>
</table>5.  Select the Reservable Module Configuration tab.

    On the form, fill in the fields.

    ![Reservable Module Configuration form showing properties.](../image/reservable-module-configuration.png)

<table id="table_imf_bxr_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Short description

</td><td>

A short description about the module.

</td></tr><tr><td>

Description

</td><td>

Detailed description about the module and the reservable items.

</td></tr><tr><td>

Available in

</td><td>

Option to specify in which reservations the module must be available.-   **Advanced reservation**: Select this option to make the module available only on the Reservation portal.
-   **Quick reservation**: Select this option to make the module available in the Reservation widget on the Workplace Service Portal homepage.
-   **Workplace Experience**: Option to display workplace option on Workplace Service Delivery for Mobile.

**Note:** The Workplace experience" is available in the Desks Reservable module level by default. If the **All day** Reservable Module checkbox is not selected, the **Workplace Experience** option is not available in **Available-In** option. Workplace users get an error when they open the In-Office Preferences page and the Workplace page from the Workplace Service Delivery for Mobile "This page cannot be loaded due to a configuration issue. Please review your configuration settings and make the necessary changes." For more information, see [Create a reservation for a day in Workplace](../../wsd-for-mobile/task/manage-schedule-emp-center.md).

</td></tr><tr><td>

Require allocation check

</td><td>

Option to check if there is an allocation mismatch between the workspace item and the logged-in user. This option appears only if you have Workplace Space Management installed.For Workplace Entities, the search results also display locations that are allocated to the parent entity.

</td></tr><tr><td>

Enable allocation duration check

</td><td>

Option to display spaces in the search results based on the start and end dates of the allocation. This field appears only when the **Require allocation check** field is selected.For recurring reservations, the allocation duration is only checked for the first occurrence.

Time-bound allocations follow only the start date and end date of the allocation, which are set in the system time zone. For more information, see [Allocate a cost center, department, or workplace entity](../../workplace-space-management/task/add-cost-center-department-floor.md).

**Note:**

-   In Workplace Space Management version 1.12.0, spaces that have the overlapping allocation and reservation time-frames are qualified for the reservation.
-   From Workplace Space Management version 1.13.0, spaces that do not have overlapping allocation and reservation time-frames are considered unallocated spaces and are qualified for reservation.


</td></tr><tr><td>

Enable restricted neighborhood rules

</td><td>

Option to apply neighbourhood restrictions on the spaces while displaying search results. The search results are displayed based on the restrictions applied on spaces. Restricted users cannot view spaces that they are not allowed to access. The restricted neighbourhoods are automatically filtered out if the logged in user is restricted.

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

Option to enable employees to search from their favorite spaces on the Now Mobile app.**Note:** This option appears only if you have Employee Center 25.0.0 and for employees who have Now Mobile app installed. Ensure that the Mobile Employee Service Portal is enabled.

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

Option to enable shift-based reservation on the module.**Note:** Recurring reservations are not support for a shift-based reservation. Employees cannot add attendees and view their availability on the reservation search page while making a reservation. For more information, see [Create a reservation](create-reservation-request-1.md) and [Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md).

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

Option to cancel a reservation if an employee does not check in within the specified time.

</td></tr><tr><td>

Enable group reservation

</td><td>

Option to allow group reservation for a selected Reservable Module Configuration. For example, **Desks**.**Note:** If the **Allow invitees** check box option is selected in the Reservation Widget Configuration, you cannot make a group reservation. The Reservation Widget Configuration tab is available in the Reservable Module.

</td></tr><tr><td>

Enable employees to make spaces as private

</td><td>

Option to enable employees to make the space details private when they make a reservation. When an employee is creating a reservation, the option **Make space details private** is displayed only if the employees are allowed to override their privacy preference for the selected space. Whether an employee can override privacy or not depends on the location privacy setup.

</td></tr><tr><td>

Enable ical generation

</td><td>

Option to enable user to generate an icalendar. **Note:** A user cannot download an iCalendar for spaces and reservations that already synchronizes with their calendar provider.

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

 **Note:** This option is not available on the Now Mobile app.

</td></tr><tr><td>

Virtual meeting provider

</td><td>

Select a virtual meeting provider to enable employees to create a virtual meeting link. If an employee selects the **Add a virtual meeting link** option, a virtual meeting link is automatically generated by the virtual meeting provider.

</td></tr><tr><td>

Allow Multiple Building Reservations

</td><td>

Option to add multiple buildings and select spaces from the buildings in a single reservation. The buildings can belong to different regions or locations and can be from different time zones. **Note:** Adding multiple buildings to a reservation is available only on the Workplace Service Portal. Recurring reservations are not supported for multi-building reservations. For more information, see [Create multi-building reservations](create-multi-building-reservation.md).

</td></tr><tr><td>

Allow all day reservation

</td><td>

Option to enable employees to reserve a reservable module for an entire day. If this option is unchecked, the **All day reservation** field is disabled.If the **Max days for multi-day** Reservable Module value is set to more than 1 day, the **All day** option is disabled on the Reservation portal. Employees can only make a single day or all day reservation in this case.

For more information, see the **Max days for multi-day** property description.

**Warning:** From Workplace Reservation Management version , the **Allow all day reservation** and **Require all day reservation** fields are merged under the **All day** field as **Enabled** and **Required** respectively.

</td></tr><tr><td>

Require all day reservation

</td><td>

Option to enforce employees to make **All day** reservation. This option depends on the **Allow All day reservation** option.

 If the **Allow all day reservation** option is disabled, this option is cleared and disabled.

 **Note:** When **Require all day reservation** is selected, employees while making or updating the reservation will find the **All day** option on the Reservation portal enabled by default.

Employees can modify the Start date but not the time on the reservation portal. For more information, see [Create a reservation](create-reservation-request-1.md)

 **Warning:** From Workplace Reservation Management version , the **Allow all day reservation** and **Require all day reservation** fields are merged under the **All day** field as **Enabled** and **Required** respectively.

</td></tr><tr><td>

All day

</td><td>

Option to enable workplace users to reserve a Reservable Modile Configuration for an entire day. For example, Desk Reservable Module Configuration.-   **Disabled**: The All day option will be disabled and is not displayed on the Reservation portal.
-   **Enabled**: The **All day** option is available and employees can reserve a space for a day.

This configuration is dependent on the \(sn\_wsd\_rsv.day\_start\) and \(sn\_wsd\_rsv.day\_end\) reservation property. For more information, see [Properties installed with Workplace Reservation Management](../reference/properties-installed-with-wsd-reservation-mgmt.md).

-   **Default**: The **All day** option is available and selected by default. However, the employees can deselect or change the timings if they want.
-   **Required**: The **All day** option is displayed as selected and cannot be changed. The **All day** field is set as mandatory.
-   **Note:** If the **All Day** check box is not selected, **Workplace Experience** option is inactive in the **Available in** Reservable Module Configuration. Workplace users get an error when they open the In-Office Preferences page and the Workplace page from Workplace Service Delivery for Mobile "This page cannot be loaded due to a configuration issue. Please review your configuration settings and make the necessary changes". For more information, see [Create a reservation for a day in Workplace](../../wsd-for-mobile/task/manage-schedule-emp-center.md).

**Warning:** From Workplace Reservation Management version , the **Allow all day reservation** and **Require all day reservation** fields are merged under the **All day** field as **Enabled** and **Required** respectively.

</td></tr><tr><td>

Max days in future

</td><td>

Option to specify the maximum number of the days in the future up to which the reservable module can be reserved. For example, if you set the max number of days in future to **90**, employees can make future reservations on this module only up to 90 days in advance. If this option is enabled, users cannot select a date beyond the specified value in **Max days in future** while making a reservation. For more information, see [Create a reservation](create-reservation-request-1.md).

On Now Mobile app, if you try to select a date too far in the future than what is specified in the **Max days in future**, no results are returned.

**Note:** **Max days in future** field indicates that the user cannot make a reservation beyond the number of days configured as the **Max days in future** value for any reservation. **Max days in future** is a reservation property and **Max number of occurrences** is a recurring reservation property. **Max days in future** value takes priority when both these options are used for the reservation.

For example, if the **Max days in future** is 90 days, then the number of occurrences in the recurring reservation can not exceed 90 days even if the user has initially configured the value for Max number of occurrences as 180 days in the Reservable module.

</td></tr><tr><td>

Allow recurring reservations

</td><td>

Option to enable employees to make recurring workplace item reservations. Select the check box to display the recurring reservation options available to users as a search parameter while making a reservation.

</td></tr><tr><td>

Auto-resolve recurring conflicts

</td><td>

Option to automatically resolve recurring reservation conflicts. This option is available when you have enabled the **Allow recurring reservations** option.The system will find an alternative space by using proximity calculation in case of conflict in reservation and will automatically resolve it. If you are using floor maps, then spaces are selected based on the proximity logic.

Option to automatically resolve recurring reservation conflicts. This option is available when you have enabled the **Allow recurring reservations** option

Resolving a conflict uses one of the following proximity calculations:

-   If a floor map is available, in that case, the application tries to find a space that is closest by using proximity.
-   If in case a floor map is not available, then the application tries to find a space within the same area or floor.

**Note:** Favorite spaces are always preferred in both the options.

-   Lastly, the application searches for an alternative space either with:
    -   same capacity
    -   more capacity
    -   less capacity
For more information, see [Create a reservation](create-reservation-request-1.md) and [Auto-resolve recurring reservations](recurring-reservations.md).

</td></tr><tr><td>

Max number of occurrences

</td><td>

Option to specify the maximum number of occurrences for recurring reservation that can be made on the reservable module. The default value is 180. This option depends on the **Allow recurring reservations** check box field. If **Allow recurring reservations** is not selected, the **Max number of occurrences** field is disabled.

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

Option to make a multi-day reservation. Employees can reserve an available space covering or spanning multiple days. For example, 5 days or more. For more information, see [Create a multi-day reservation](create-multi-day-reservation.md).Default value for this Reservable Module property is 1. To make a single day reservation, set the value to 1. Value 0 \(zero\) is not allowed.

When the **Max days for multi-day** value is more than 1, the **All day** option is disabled on the Reservation portal while making a reservation.

**Note:** The number of days for this property must not exceed the **Max days in future** value on the Reservable Module.

</td></tr><tr><td>

Enable browse near a person

</td><td>

Option to enable users to search for spaces near a person. When a user searches for a space near a person, the available spaces located on the user's floor are displayed. The display criteria are also based on the nearby area of the space or tags assigned to the spaces.**Note:** The search limit criteria is not applicable if the option is enabled.

</td></tr><tr><td>

Max number of days for browse near a person

</td><td>

Option to specify the number of days employees can reserve a space near a colleague. Admins can configure the maximum number of days an employee would like to reserve a space near a colleague using this property.Default value is 7. Admins can change this value to more than 7 days and enable employees to select the max number of days they would like to book a seat near a team member or a colleague. For more information, see [Create a reservation](create-reservation-request-1.md).

**Note:** This field is displayed only when the **Enable browse near a person** Reservable module property is enabled on the Reservable Module.

The number of days provided for this property cannot be 0 or a negative number \(for example, -10\). The number of days for this property must not exceed the **Max days in future** value on the Reservable Module.

</td></tr><tr><td>

Enable facet filter

</td><td>

Option to enable facet filter on the workplace items. If the select this option, the filter options are displayed based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.

</td></tr><tr><td>

Search limit

</td><td>

Option to specify the maximum limit of search results when an employee searches for a workplace location.

</td></tr></tbody>
</table>6.  Select the Reservation Widget Configuration tab.

    On the form, fill in the fields.

    ![Reservable Module Widget Configuration properties.](../image/rsv-module-allow-attendees-search.png)

<table id="table_rkb_rxr_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires subject

</td><td>

Option to make a reservation subject required before making a reservation.

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

Allow attendees-based search

</td><td>

Option to add meeting attendees and search for their availability on the Make a reservation portal page. Employees can collaborate with attendees effectively by adding them to their meetings. This option is dependent on the **Allow Invitees** reservable module configuration. If the **Allow Invitees** option is not enabled, this option is unavailable for selection and cannot be enabled.

The ability to search and add colleagues or attendees based on their availability is supported only for Microsoft Exchange Online.

**Note:** Colleagues can be added on the reservation portal search page. The application retrieves their availability to add them as reservation attendees. Guests can be added on the reservation details page after you've selected a space. For more information, see [Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md).

</td></tr><tr><td>

Allow invitees

</td><td>

Option to enable employees to invite attendees to their reservation. Employees can invite co-workers and also external visitors.-   If the **Allow invitees** check box is selected, the **Display number of attendees** and **Enable Group Reservations** check box options are unselected by default.
-   If **Display number of attendees** is selected, the **Allow invitees** check box selection is unselected by default.


</td></tr><tr><td>

Display number of attendees

</td><td>

Option to enable employees to specify the number of attendees while making a reservation. If the option is not selected, then the number of attendees is automatically set to **1**. -   If the **Allow invitees** check box is selected, the **Display number of attendees** and **Enable Group Reservations** check box options are unselected by default.
-   If **Display number of attendees** is selected, the **Allow invitees** check box selection is unselected by default.


</td></tr><tr><td>

Display on behalf of

</td><td>

Option to enable employees to specify on whose behalf they are making a reservation. The option is enabled by default. An error is displayed if the option is disabled.

</td></tr><tr><td>

Display sensitivity

</td><td>

Option to enable employees to set the sensitivity of the reservation. They can set a reservation to **Normal** or **Private**. If the option is not selected, the sensitivity is set to **Normal** and the subject will be visible to others.

</td></tr><tr><td>

Allow reservation message

</td><td>

Option to add notes to a meeting and attach images while making a reservation. The notes and images can be shared with the meeting invitees.**Note:** When calendar sync is enabled for a space, the message or notes will also be added to the body when we sync the reservation.

For Now Mobile app, the message is displayed on the summary page but employees cannot add or edit a message.

For more information, see [Create a reservation](create-reservation-request-1.md).

.

</td></tr><tr><td>

Additional details record producer

</td><td>

Option to link to the record producer that you have configured with additional fields. You can display additional fields on the reservation form. For more information, refer to [Configure reservable module with additional details](configure-reservable-module-with-custom-fields.md).

</td></tr><tr><td>

Show as

</td><td>

Option to specify what status must the reservation show on the employee's calendar when a reservation is synchronized. This field appears only if Workplace Calendar Synchronization is installed. -   **Busy**: The reservation will be displayed in the Employee's calendar with a Busy status. The employee's calendar is blocked during the reservation duration.
-   **Free**: The reservation will be displayed in the Employee's calendar with a Free status. The employee's calendar will not be blocked during the reservation duration.
 **Note:** For the **Show as** feature to work correctly, you must have the following versions of the connections:

-   For Microsoft, you must have Microsoft Exchange Online spoke version 3.2.4.
-   For Google Calendar, you must have the Google Calendar version 2.3.1.


</td></tr></tbody>
</table>    The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Widget instances. The start time and end time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes. For more information see, [https://www.servicenow.com/docs/bundle/xanadu-platform-user-interface/page/build/service-portal/concept/c\_ConfigureWidgetInstances.html](https://www.servicenow.com/docs/bundle/xanadu-platform-user-interface/page/build/service-portal/concept/c_ConfigureWidgetInstances.html)

7.  Click **Submit**.


## Result

The Reservable module configuration is added to the application. The reservable items are available to employees based on the filter conditions and properties that are configured. The filter conditions can be applied in the Reservable Table Configuration for a location.

-   **[Configure a reservable module to group spaces in an area](config-rsv-mod-for-neighspace.md)**  
Create a reservable module to group spaces in an area. Enable employees to reserve a space in an area.
-   **[Add workplace locations to a reservable module](add-allowed-buildings-to-reservable-module.md)**  
Configure workplace locations that must be available to users for reservation when they select a reservable module. Restrict the usage of a workplace by adding only those workplaces that are can be reserved.
-   **[Generate and print a QR code for a reservable module](generate-qr-code-for-rsv-module.md)**  
Generate and print a QR code for an entire reservable module. Place the QR codes at reservable workplace locations so that employees can scan the code, make a reservation, or perform reservation-related actions.
-   **[Create a record producer to add additional details](create-a-record-producer-to-add-additional-fields.md)**  
Configure a record producer with additional details and add it to the reservable module. The fields configured for additional details will be displayed to the employee when they make a reservation.
-   **[Configure reservable module with additional details](configure-reservable-module-with-custom-fields.md)**  
The application enables you configure a reservable module with additional details based on your organization's requirements.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

