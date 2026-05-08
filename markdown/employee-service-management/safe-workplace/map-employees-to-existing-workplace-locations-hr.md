---
title: Map designated workspaces to user profiles
description: Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mapping employees to their designated workspaces, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Map designated workspaces to user profiles

Map existing designated workspaces to employee user profiles in Workplace Core. This mapping is used to automatically allocate workspaces for employees so they don't have to select a workspace manually when requesting a reservation.

## Before you begin

-   Ensure that your workplace administrator has completed setting up your workplace data. For more information, see [Providing your workplace data](../../workplace-service-delivery/concept/providing-your-workplace-data-wsd.md).
-   Ensure that you have the designated workplace information for all the employees.
-   You can also Navigate to the User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table by entering `sn_wsd_core_workplace_profile.list` in the navigation filter.

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

Workplace location

</td><td>

Designated workplace of the employee.

</td></tr><tr><td>

Active

</td><td>

Option for indicating that this workplace mapping is active.

</td></tr><tr><td>

Enable employee location privacy

</td><td>

Option to set location privacy preference for the workplace profile. Note the following:-   Set this option only if you want to have a different privacy setup for the workplace profile.
-   By default, the location privacy preference that is set on the building to which the workplace profile is assigned is considered.
-   In case, the building doesn't have any location privacy preference, preference set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered.
-   The field is set to **None** by default.
 For more information about each field, refer to [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md)

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Repeat the procedure for all the employees of the workplace that you manage.


## Result

The User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table is populated with all the new profiles.

**Parent Topic:**[Mapping employees to their designated workspaces](../concept/mapping-employees-to-existing-work-locations.md)

