---
title: Properties installed with Workplace Concierge
description: Customize the system properties available with Workplace Concierge as required.
locale: en-US
release: zurich
product: Workplace Concierge
classification: workplace-concierge
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Concierge

Customize the system properties available with Workplace Concierge as required.

Configure Workplace Concierge properties for improved workspace suggestions. The preferred workplace suggestions are shown to an employee in the search results. Employees can select a suggested workspace while reserving a space using the Workplace Service Delivery for Mobile app. The workspace suggestions are also based on user workplace profile location preferences, employee presence configuration, user space table and space suggestions table configuration, and future and past reservations.

Following properties are installed with Workplace Concierge.

**Note:** The Workplace Concierge properties are available in **All** &gt; **Workplace Concierge** &gt; **Administration** &gt; **Properties.**. These properties are also available in the the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter context menu.

<table id="table_cqn_gcl_kmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Collaborators filter \[sn\_wsd\_concierge.collaborators\_filter\]

</td><td>

Property to add a collaborator for a workplace employee. Apply condition filters as required to add workplace users as collaborators. Default value is set to true.

</td></tr><tr><td>

Allow user to have parallel reservation from desk suggestions card on workplace page \[sn\_wsd\_concierge.allow\_overlapping\_reservations\]

</td><td>

Property to allow a parallel or multiple desk reservations for a day from the Desk suggestions card in Workplace Service Delivery for Mobile. By default, this property is set to true. If it is set to false, employees cannot have multiple or parallel desk reservations for a day using the Desk Suggestions card. After reserving a space, they will not see the Space Suggestions for other workspaces.

By default, allow\_overlapping\_reservations is set to false. If this property is not selected or is false, after making a reservation, Space Suggestions card is hidden. A message is displayed "Reservation created for your in-office day on &lt;calendar date&gt;, &lt;calendar weekday&gt;." Changing the reservation date shows Space suggestions facet. If this property is selected or true, Space Suggestions facet is visible. For more information, see [Create a reservation for a day in Workplace](../../wsd-for-mobile/task/manage-schedule-emp-center.md).

</td></tr><tr><td>

Specifies the number of past days to consider when generating reservation suggestions for the user

\[sn\_wsd\_concierge.suggestions\_reservation\_past\_days\_to\_consider\]

</td><td>

Specifies the maximum number of past days the application considers when proposing a workspace to an employees. Max value is 90 days. Allowing users to have parallel reservations from the Space suggestions card can be set to True or False \(Check or Uncheck\). For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

</td></tr><tr><td>

List of space types that are used when suggesting available spaces to employees to reserve.

\[sn\_wsd\_concierge.suggestions\_space\_types\]

</td><td>

Space type record that is used while suggesting spaces to an employee for reservation. By default, Space type suggestion is fetched from the **Workspace/Desk** Reservable Module Configuration.The list of space types determines which spaces are suggested to employees for reservation. For example: 5f017383eb512010b89bfdfc9c5228c8.

By default, the **Desks** Reservable Module and Workspace/Desk \(space type\) are shown. Employees can see suggestions for locations and workspaces included in the Desks Reservable Module Configuration on the Workplace page. For more information, see Workplace Service Delivery for Mobile.

To include other Reservable Module Configuration, such as Rooms or Meeting rooms, add the Sys ID of the Rooms or Meeting rooms this property. This property can take comma separated values. For example:

List of space types: 5f017383eb512010b89bfdfc9c5228c8,20713b83eb512010b89bfdfc9c522899

Set the **Available-in** Reservable Module Configuration property to **Workplace experience** in the Reservable module Configuration. Make sure **All day** is enabled at the Reservable module level. By default, this property is enabled for the **Desks** Reservable Module Configuration.

For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md) and [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

For more information, see:

-   [Add a space type configuration](../../workplace-service-delivery/task/add-space-type-configuration-wsd.md)
-   [Add a space using Workplace Space Management](../../workplace-space-management/task/add-a-space.md)
-   [Space suggestion Configuration](../task/space-suggestion-configuration.md)
-   [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

</td></tr><tr><td>

The maximum number of days an employee can select at once through the Workplace experience \[sn\_wsd\_concierge.workplace\_day\_selection\_limit\]

</td><td>

Option to enter the maximum number of days an employee can select on the calendar component in the Workplace page. Default value is 10 days. Negative value \(zero\) is not supported. For more information, see [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

When this property is set, the **Select multiple days** toggle button is available on the Workplace page. Employees can select multiple days on the calendar for making bulk reservations. For example, if this property is set to 5, employees can see 5 In-office days selected on the calendar.

The employee can auto-select days or dates on the calendar until the maximum allowed selected days in this property.

If there is no date selected, the system shall select the first allowed \(possible\) date and try to select all days until the maximum selection limit.

When an employee removes a date from the calendar, the suggestion is removed from the Space Suggestions list view.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Concierge reference](../concept/workplace-concierge-reference.md)

