---
title: Vaccine Administration Management system properties
description: Vaccine Administration Management booking uses the following system properties. Users with the admin role can access the property settings by navigating to All Vaccine Administration Management Administration Properties .
locale: en-US
release: yokohama
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Vaccine Administration Management system properties

Vaccine Administration Management booking uses the following system properties. Users with the admin role can access the property settings by navigating to **All** &gt; **Vaccine Administration Management** &gt; **Administration** &gt; **Properties**.

<table id="table_z52_hsw_p4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_vaccine\_sm.enable\_appointment\_slot\_choice

</td><td>

Enable or disable appointment slot choice.

 When set to **true**, users can choose the slot. When set to **false**, the system books an appointment automatically.

 The default value is **false**.

</td></tr><tr><td>

sn\_vaccine\_sm.self\_booking\_slots\_fetched

</td><td>

Set the number of slots fetched by the system to book an appointment in user self-booking. The higher value reduces any chance of failed appointments in high concurrency scenarios.

 The default value is **1**.

**Note:** The system property only applies if the **sn\_vaccine\_sm.enable\_appointment\_slot\_choice** value is **false**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.distance\_unit

</td><td>

Define the unit of measurement for the distance considered for vaccine appointment mass booking. The options are **mi** or **km**.

 The default value is **mi**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.max\_distance

</td><td>

Set the maximum distance, in miles, that is searched for an available vaccination location if there’s no appointment slot available at the user’s preferred center.

 The default value is **50**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.max\_locations

</td><td>

Set the maximum number of alternate locations that are searched for a vaccination if there’s no appointment slot available at the user’s preferred location. A higher value for this property increases the time that it takes to complete mass booking.

 The default value is **5**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.default\_program

</td><td>

Define the default program for the Vaccine Administration Management portal.

</td></tr><tr><td>

sn\_vaccine\_sm.book\_subsequent\_doses

</td><td>

Enable booking for all doses of the vaccine, for both mass booking and self-service, or enable booking for the first dose, with subsequent appointments booked after the first dose is administered.

 When set to **true**, appointments are booked for all doses of the vaccine, both in mass scheduling and self-service. When set to **false**, only the appointment for the first dose is booked and subsequent appointments are booked only after the previous dose is administered.

 The default value is **true**.

 For more information about booking subsequent doses, see [Book appointments for subsequent doses after a previous dose is complete](../task/schedule-second-appointment-after-completion-of-first.md).

</td></tr><tr><td>

sn\_vaccine\_sm.enable\_vam\_appointment\_config

</td><td>

Enable Vaccine Administration Management location-specific appointment scheduling configuration.

 The default value is **true**.

 For more information about enabling location-specific appointment configuration, see [Configure advanced appointment scheduling for a center](../task/configure-location-level-weekly-schedule-config.md).

</td></tr><tr><td>

sn\_vaccine\_sm.fetch\_next\_available\_slot

</td><td>

Enable or disable fetching for the next available slot when opening the appointment booking calendar.

 The default value is **true**.

</td></tr><tr><td>

sn\_vaccine\_sm.strict\_check\_lead\_max\_time

</td><td>

Display the time after which the first available appointment slot is shown to the user.

 When set to **true**, slots for subsequent doses are calculated to accuracy, measured in seconds, using lead or max times. When set to **false**, the second slot can be booked at any time.

 For example, if the first dose is administered on June 1, 5:00 PM and the lead time is 21 days, the second slot can be booked after June 22, 5:00 PM. However, if the property is **false**, the second slot can be booked at any time on June 22.

 This system property affects mass booking.

 The default value is **true**.

</td></tr><tr><td>

sn\_vaccine\_sm.enable\_self\_registration

</td><td>

Enable or disable self-registration for booking appointments.

 When set to **true**, the user can register and sign up for the vaccine. When set to **false**, only existing users can sign up and book appointments.

 The default value is **true**.

</td></tr><tr><td>

sn\_vaccine\_sm.show\_location\_filters

</td><td>

Show or hide the location filters in the Schedule your vaccination page.

 When set to **true**, the list of preferred vaccination sites is filtered automatically using the personal information shared by the user. However, you can also look for other vaccination sites based on your preferred choice of state, city, or zip code.

 ![Portal view for scheduling a vaccination when the location filters are enabled, allowing users to select their state, city, zip code, and preferred vaccination site.](../image/vam-properties-location-filters.png)

 When set to **false**, the location filters are inactive.

 The default value is **true**.

</td></tr><tr><td>

sn\_vaccine\_sm.mass\_booking\_parallelism

</td><td>

Configure the number of parallel queues used to process mass booking.

 The enabled values are **1 to 8**.

**Note:** A maximum of 8 queues can be used for mass booking. Even if a user with the admin role sets the property to a value greater than **8**, only 8 queues are created.

 The default value is **4**.

 For more information about enabling mass booking parallel processing, see [Manage high number of concurrent bookings](managing-high-number-of-concurrent-booking.md).

</td></tr><tr><td>

sn\_vaccine\_sm.search\_assist\_accessibility

</td><td>

Minimize the search assist section and view the search results even at 200% zoom. To expand the search assist section, click **Show search assist**.

 When set to **true**, clicking **Search** automatically minimizes the search assist section. When set to **false**, the system returns to its default behavior.

</td></tr><tr><td>

sn\_vaccine\_sm.enable\_inventory\_management

</td><td>

Enable scheduling based on available inventory for a program location center.

 The default value is **false**.

 For more information about enabling inventory management, see [Configure inventory-based scheduling for a center](../task/configure-scheduling-by-inventory.md).

</td></tr><tr><td>

sn\_vaccine\_sm.im\_batch\_distribution\_day\_count

</td><td>

Set the number of days to distribute a supply lot. You can distribute the inventory evenly over a specified date range.

 The default value is **7**.

</td></tr><tr><td>

sn\_vaccine\_sm.enable\_multi\_vaccine

</td><td>

Change the order of method selection while scheduling your vaccinations.

 When set to **true**, the auto-selected method is based on the lowest method order and inventory availability. When set to **false**, the method with the lowest order is selected.

**Note:** The system property only applies if the **sn\_vaccine\_sm.enable\_inventory\_management** value is **true**.

 The default value is **false**.

</td></tr><tr><td>

sn\_vaccine\_sm.multi\_vaccine\_availability\_check\_days\_count

</td><td>

Set the number of days to check for the availability in the method selection.

**Note:** The system property only applies if the **sn\_vaccine\_sm.enable\_multi\_vaccine** value is **true**.

 The default value is **7**.

</td></tr><tr><td>

sn\_vaccine\_sm.allow\_user\_selection\_of\_vaccine\_method

</td><td>

Enable or disable multi-vaccine method selection.

 When set to **true**, users can choose the method while scheduling and rescheduling their appointments. When set to **false**, the system auto-selects the method based on the configuration of the **sn\_vaccine\_sm.enable\_multi\_vaccine** system property.

 The default value is **false**.

</td></tr><tr><td>

sn\_vaccine\_sm.covid.test.valid.days

</td><td>

Set the maximum duration in days that is used for infectious diseases, such as COVID-19 test report validity.

 The default value is **3**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.create\_immunization\_on\_self\_report

</td><td>

Enable or disable the immunization record that is generated on COVID-19 vaccine self-report submission.

 The default value is **false**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.show\_programs\_proof

</td><td>

Define the list of programs that require proof of vaccination.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.program\_covid\_sys\_id

</td><td>

Define the system identifier of the infectious diseases, such as COVID-19 vaccination program.

</td></tr><tr><td>

sn\_vaccine\_sm.enable\_cache

</td><td>

Enable or disable scoped cache for use with the application.

 When set to **true**, scoped cache is enabled. When set to **false**, data isn’t cached and instead queried from the database directly.

 The default value is **true**.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Vaccine Administration Management](vaccine-mgmt-config.md)

