---
title: Map designated workspaces to user profiles
description: Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mapping employees to their designated workspaces, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Map designated workspaces to user profiles

Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.

## Before you begin

-   Ensure that your workplace administrator has completed setting up your workplace data. For more information, see [Providing your workplace data](../concept/providing-your-workplace-data-wsd.md).
-   Ensure that you have the designated workplace information for all the employees.
-   You can also navigate to the User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table by entering `sn_wsd_core_workplace_profile.list` in the navigation filter.

    **Note:** From Workplace Core version 2.16.1, the workplace user profiles are created in the Workplace Profile Location Assignment \[sn\_wsd\_core\_workplace\_profile\_location\] table. A new field **Is Primary** is added in the table so that you can specify if a location is the primary location when there are multiple locations. In case of existing user profiles created in the User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table, a fix script will run and will automatically consider the latest workplace location added to the profile as the primary workplace location.


**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** is no longer available. A new allocation type, **Workplace entity** is introduced that provides more advantages.

Role required: sn\_wsd\_core.admin or sn\_wsd\_core.workplace\_manager

## About this task

Create a mapping for all employees and their designated workplaces. You can also perform an easy import of your employee workplace data. For more information, see Easy import.

## Procedure

1.  Navigate to **All** &gt; **Workplace Safety Management** &gt; **Administration** &gt; **Workplace profiles**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_rxs_xdv_zlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee

</td><td>

Employee for whom you want to create a workplace mapping.

</td></tr><tr><td>

Workplace entity

</td><td>

Workplace entity of your workplace to which the employee belongs. You can view this option only if you have installed the Workplace Space Management plugin and the view is set to **Space management** view.

</td></tr><tr><td>

Primary Workplace location

</td><td>

Primary or the main workplace location of the employee. The location is automatically set based on the Workplace Profile Location Assignment that is set as true. If there are no workplace locations assigned to the employee, then the field is set to read-only and empty.

</td></tr><tr><td>

Active

</td><td>

Option for indicating that this workplace mapping is active.

</td></tr><tr><td>

Enable employee location privacy

</td><td>

Option to set location privacy preference for the workplace profile. Note the following:**Note:** The field will be set to read-only and **None** if there are no workplace locations assigned to the employee. Otherwise, if a primary workplace location is set, then the privacy set on the primary workplace location is considered.

-   Set this option only if you want to have a different privacy setup for the workplace profile.
-   By default, the location privacy preference that is set on the building to which the workplace profile is assigned is considered.
-   In case, the building doesn't have any location privacy preference, preference set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered.
-   The field is set to **None** by default.
 For more information about each field, refer to [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md)

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Repeat the procedure for all the employees of the workplace that you manage.


## Result

The User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table is populated with all the new profiles.

**Parent Topic:**[Mapping employees to their designated workspaces](../concept/mapping-employees-to-existing-work-locations-wsd.md)

